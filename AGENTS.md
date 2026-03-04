# Drakula API Documentation Guidelines

## About This Project

This is the official API documentation for the Drakula trading platform, built on [Mintlify](https://mintlify.com).

### Key Features
- **Real-time API Documentation**: Automatically generated from OpenAPI specifications
- **Interactive Examples**: Live code samples in multiple languages
- **Searchable Reference**: Full-text search across all endpoints
- **Version Control**: Documentation updates with API changes

### Technical Stack
- **Framework**: Mintlify
- **Content Format**: MDX files with YAML frontmatter
- **Configuration**: `docs.json` for site settings and navigation
- **API Spec**: `openapi.json` for endpoint documentation

## Development Workflow

### Local Development
```bash
# Install Mintlify CLI
npm i -g mint

# Start local preview server
mint dev

# Check for broken links
mint broken-links
```

### Content Updates
1. **API Endpoints**: Update `openapi.json` and regenerate documentation
2. **Guides**: Edit MDX files in appropriate directories
3. **Navigation**: Update `docs.json` navigation structure
4. **Styling**: Modify `docs.json` theme and color settings

## Terminology Standards

### Platform Terminology
- **Token**: Digital asset traded on the platform (not "coin" or "currency")
- **Pair**: Trading pair (e.g., ETH/USDC)
- **Swap**: Token exchange transaction
- **Position**: Active trade with entry and potential exit targets
- **Intention**: Trading strategy configuration (Auto Buy or Copy Trade)
- **Slot**: User's trading wallet/smart contract
- **Router**: DEX aggregator or liquidity source

### API Terminology
- **Endpoint**: API URL path (e.g., `/api/v1/user/profile`)
- **Parameter**: Input to API call (path, query, or body)
- **Response**: JSON output from successful API call
- **Error**: Standardized error response format
- **Authentication**: Bearer token-based access control
- **Rate Limit**: Request throttling per minute

### User Roles
- **Trader**: User executing trades
- **Caller**: Social media influencer making token calls
- **Follower**: User copying trades from callers
- **Developer**: API integration developer
- **Administrator**: Platform admin with elevated privileges

## Style Guidelines

### Voice and Tone
- **Use active voice**: "The API returns data" not "Data is returned by the API"
- **Second person address**: Address the reader as "you"
- **Professional yet approachable**: Technical but not overly formal
- **Concise explanations**: One idea per sentence, avoid unnecessary complexity

### Content Structure
- **Sentence case for headings**: "Getting started" not "Getting Started"
- **Consistent formatting**:
  - **Bold** for UI elements: Click **Generate Token**
  - `Code formatting` for endpoints, parameters, and code
  - *Italics* for emphasis or new terms
- **Progressive disclosure**: Start simple, add complexity gradually
- **Practical examples**: Show real-world usage scenarios

### Code Examples
- **Multiple languages**: Provide examples in Python, JavaScript, and cURL
- **Complete examples**: Include imports, setup, and error handling
- **Realistic data**: Use realistic token addresses and amounts
- **Security warnings**: Always include security best practices
- **Environment variables**: Show proper credential management

### API Documentation Standards
- **Endpoint sections**:
  1. **Title**: Clear, descriptive endpoint name
  2. **HTTP Method & Path**: `GET /api/v1/user/profile`
  3. **Description**: Brief overview of endpoint purpose
  4. **Authentication**: Required permissions and scopes
  5. **Parameters**: Table with name, type, required, description
  6. **Responses**: Success and error response examples
  7. **Code Examples**: Working examples in multiple languages
  8. **Notes**: Additional considerations and limitations

- **Parameter tables**:
  ```
  | Name | Type | In | Required | Description | Example |
  |------|------|----|----------|-------------|---------|
  ```

- **Response examples**: Include both success and error responses
- **Rate limiting**: Always mention rate limits for endpoints

## Content Boundaries

### What to Document
- **Public API endpoints**: All endpoints available to developers
- **Authentication methods**: Token generation and usage
- **Rate limits**: Request limitations and best practices
- **Error handling**: Common errors and resolution steps
- **Integration patterns**: Recommended implementation approaches
- **Security guidelines**: Best practices for secure integration
- **Migration guides**: Version updates and breaking changes

### What NOT to Document
- **Internal endpoints**: Admin-only or internal system APIs
- **Security vulnerabilities**: Specific exploit details
- **Unreleased features**: Endpoints in development or testing
- **Partner-specific integrations**: Custom implementations for specific partners
- **Pricing details**: Exact fee structures (link to pricing page instead)
- **Legal compliance**: Regulatory requirements (link to legal docs)

### Sensitive Information
- **Never include**:
  - Real API tokens or private keys
  - User personal data in examples
  - Internal IP addresses or domains
  - Database schemas or internal structures
  - Security configuration details

## Quality Standards

### Accuracy
- All code examples must be tested and functional
- Endpoint documentation must match actual API behavior
- Version numbers must be current and accurate
- Deprecated features must be clearly marked

### Consistency
- Use consistent terminology across all documentation
- Maintain uniform formatting and structure
- Follow established patterns for similar content types
- Keep navigation logical and predictable

### Completeness
- Every endpoint must have complete documentation
- All parameters must be described
- Error responses must be documented
- Authentication requirements must be specified
- Rate limits must be stated

### Accessibility
- Use descriptive link text (not "click here")
- Provide alt text for all images
- Ensure sufficient color contrast
- Use semantic HTML structure
- Support keyboard navigation

## Review Process

### Content Review
1. **Technical accuracy**: Verify API behavior matches documentation
2. **Clarity**: Ensure explanations are understandable
3. **Completeness**: Check for missing information
4. **Consistency**: Verify terminology and formatting
5. **Examples**: Test all code samples

### Update Frequency
- **Major API changes**: Documentation updated within 24 hours
- **New features**: Documentation released with feature launch
- **Bug fixes**: Documentation updated as needed
- **Quarterly review**: Comprehensive review every 3 months

## Resources

### Internal Resources
- **API Specifications**: `openapi.json`
- **Design System**: Brand colors and components in `docs.json`
- **Template Files**: Standard documentation templates
- **Example Repository**: https://github.com/drakula/examples

### External Resources
- **Mintlify Documentation**: https://mintlify.com/docs
- **OpenAPI Specification**: https://spec.openapis.org/oas/v3.1.0
- **MDX Documentation**: https://mdxjs.com
- **API Style Guide**: https://github.com/WhiteHouse/api-standards

### Support Channels
- **Documentation Issues**: GitHub repository issues
- **API Support**: api-support@drakula.com
- **Developer Community**: Discord community channel
- **Emergency Updates**: Status page notifications

## Version History

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| 1.0.0 | 2024-01-15 | Initial documentation setup | Engineering Team |
| 1.1.0 | 2024-01-20 | Added API endpoint documentation | Documentation Team |
| 1.2.0 | 2024-01-25 | Updated style guidelines and examples | Content Team |

---

*Last updated: January 25, 2024*
*Next review: April 25, 2024*
# GetTest TypeScript SDK

test

## Overview

The GetTest API allows you to retest it.

## Installation

```bash
npm install @test-sdk-123/sdk-typescript --save
```

## Configuration

```typescript
import { Configuration, EchoApi } from '@test-sdk-123/sdk-typescript';

// Create configuration with API key
const config = new Configuration({
  headers: {
    'api-key': 'your_api_key_here'
  }
});

// Create API client
const api = new EchoApi(config);
```

## Example Request

```typescript
// Get brand data by domain
const response = await api.echo("test");

// Access brand data
console.log('Brand:', response.brand.name);
console.log('Logo:', response.images.logos[0].url);
console.log('Primary Color:', response.colors.primary[0].hex);
```

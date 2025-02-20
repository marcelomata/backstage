## API Report File for "@backstage/plugin-rollbar-backend"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { Config } from '@backstage/config';
import express from 'express';
import { Logger } from 'winston';

// Warning: (ae-missing-release-tag) "createRouter" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export function createRouter(options: RouterOptions): Promise<express.Router>;

// Warning: (ae-missing-release-tag) "getRequestHeaders" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export function getRequestHeaders(token: string): {
  headers: {
    'X-Rollbar-Access-Token': string;
  };
};

// Warning: (ae-missing-release-tag) "RollbarApi" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export class RollbarApi {
  constructor(accessToken: string, logger: Logger);
  // (undocumented)
  getActivatedCounts(
    projectName: string,
    options?: {
      environment: string;
      item_id?: number;
    },
  ): Promise<
    {
      timestamp: number;
      count: number;
    }[]
  >;
  // (undocumented)
  getAllProjects(): Promise<
    {
      id: number;
      name: string;
      accountId: number;
      status: string;
    }[]
  >;
  // (undocumented)
  getOccuranceCounts(
    projectName: string,
    options?: {
      environment: string;
      item_id?: number;
    },
  ): Promise<
    {
      timestamp: number;
      count: number;
    }[]
  >;
  // (undocumented)
  getProject(projectName: string): Promise<{
    id: number;
    name: string;
    accountId: number;
    status: string;
  }>;
  // (undocumented)
  getProjectItems(projectName: string): Promise<{
    items: RollbarItem[];
    page: number;
    totalCount: number;
  }>;
  // (undocumented)
  getTopActiveItems(
    projectName: string,
    options?: {
      hours: number;
      environment: string;
    },
  ): Promise<
    {
      item: {
        id: number;
        counter: number;
        environment: string;
        framework: RollbarFrameworkId;
        lastOccurrenceTimestamp: number;
        level: number;
        occurrences: number;
        projectId: number;
        title: string;
        uniqueOccurrences: number;
      };
      counts: number[];
    }[]
  >;
}

// Warning: (ae-missing-release-tag) "RouterOptions" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface RouterOptions {
  // (undocumented)
  config: Config;
  // (undocumented)
  logger: Logger;
  // (undocumented)
  rollbarApi?: RollbarApi;
}

// Warnings were encountered during analysis:
//
// src/api/RollbarApi.d.ts:20:9 - (ae-forgotten-export) The symbol "RollbarItem" needs to be exported by the entry point index.d.ts
// src/api/RollbarApi.d.ts:32:13 - (ae-forgotten-export) The symbol "RollbarFrameworkId" needs to be exported by the entry point index.d.ts
```

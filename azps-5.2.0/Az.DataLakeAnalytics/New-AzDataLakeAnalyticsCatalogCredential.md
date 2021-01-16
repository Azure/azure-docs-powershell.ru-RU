---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406583"
---
# <span data-ttu-id="af2cf-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="af2cf-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="af2cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="af2cf-103">Создает учетные данные каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="af2cf-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="af2cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af2cf-104">SYNTAX</span></span>

### <span data-ttu-id="af2cf-105">CreateByHostNameAndPort (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af2cf-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af2cf-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="af2cf-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af2cf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af2cf-107">DESCRIPTION</span></span>
<span data-ttu-id="af2cf-108">Новый New-AzDataLakeAnalyticsCatalogCredential создает учетные данные для подключения к внешним источникам данных в каталоге Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="af2cf-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="af2cf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af2cf-109">EXAMPLES</span></span>

### <span data-ttu-id="af2cf-110">Пример 1. Создание учетных данных для каталога, указыващего хост и порт</span><span class="sxs-lookup"><span data-stu-id="af2cf-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="af2cf-111">Эта команда создает указанные учетные данные для указанной учетной записи, базы данных, хоста и порта с помощью протокола https.</span><span class="sxs-lookup"><span data-stu-id="af2cf-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="af2cf-112">Пример 2. Создание учетных данных для каталога с полным URI</span><span class="sxs-lookup"><span data-stu-id="af2cf-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="af2cf-113">Эта команда создает указанные учетные данные для указанной учетной записи, базы данных и внешнего источника данных URI.</span><span class="sxs-lookup"><span data-stu-id="af2cf-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="af2cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af2cf-114">PARAMETERS</span></span>

### <span data-ttu-id="af2cf-115">-Account</span><span class="sxs-lookup"><span data-stu-id="af2cf-115">-Account</span></span>
<span data-ttu-id="af2cf-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="af2cf-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="af2cf-117">-Credential</span></span>
<span data-ttu-id="af2cf-118">Указывает имя пользователя и соответствующий пароль учетных данных.</span><span class="sxs-lookup"><span data-stu-id="af2cf-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="af2cf-119">-CredentialName</span></span>
<span data-ttu-id="af2cf-120">Указывает имя и пароль учетных данных.</span><span class="sxs-lookup"><span data-stu-id="af2cf-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="af2cf-121">-DatabaseHost</span></span>
<span data-ttu-id="af2cf-122">Указывает имя внешнего источника данных, к который можно подключить учетные данные, в формате mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="af2cf-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af2cf-123">-DatabaseName</span></span>
<span data-ttu-id="af2cf-124">Имя базы данных в учетной записи Data Lake Analytics, в которой будут храниться учетные данные.</span><span class="sxs-lookup"><span data-stu-id="af2cf-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2cf-125">-DefaultProfile</span></span>
<span data-ttu-id="af2cf-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af2cf-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-127">-Port</span><span class="sxs-lookup"><span data-stu-id="af2cf-127">-Port</span></span>
<span data-ttu-id="af2cf-128">Номер порта, используемый для подключения к указанному databaseHost с использованием этих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="af2cf-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="af2cf-129">-Uri</span></span>
<span data-ttu-id="af2cf-130">Указывает полный URI внешнего источника данных, к котором могут подключаться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="af2cf-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af2cf-131">-Confirm</span></span>
<span data-ttu-id="af2cf-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af2cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2cf-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2cf-134">CommonParameters</span></span>
<span data-ttu-id="af2cf-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af2cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2cf-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2cf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2cf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af2cf-137">INPUTS</span></span>

### <span data-ttu-id="af2cf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="af2cf-138">System.String</span></span>

### <span data-ttu-id="af2cf-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="af2cf-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="af2cf-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="af2cf-140">System.Uri</span></span>

### <span data-ttu-id="af2cf-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="af2cf-141">System.Int32</span></span>

## <span data-ttu-id="af2cf-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af2cf-142">OUTPUTS</span></span>

### <span data-ttu-id="af2cf-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="af2cf-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="af2cf-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af2cf-144">NOTES</span></span>

## <span data-ttu-id="af2cf-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af2cf-145">RELATED LINKS</span></span>
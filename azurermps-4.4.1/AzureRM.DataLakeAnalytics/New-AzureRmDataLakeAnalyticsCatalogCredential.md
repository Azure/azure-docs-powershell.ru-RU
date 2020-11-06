---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 1668ca10c8c3425bea7c4082033abb19f8de7306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559867"
---
# <span data-ttu-id="23972-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="23972-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="23972-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23972-102">SYNOPSIS</span></span>
<span data-ttu-id="23972-103">Создание учетных данных нового каталога данных Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23972-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23972-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23972-104">SYNTAX</span></span>

### <span data-ttu-id="23972-105">Укажите имя узла и порт (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="23972-105">Specify host name and port (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23972-106">Укажите полный URI</span><span class="sxs-lookup"><span data-stu-id="23972-106">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23972-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23972-107">DESCRIPTION</span></span>
<span data-ttu-id="23972-108">Командлет New-AzureRmDataLakeAnalyticsCatalogCredential создает новые учетные данные для использования в каталоге Azure Data Lake Analytics для подключения к внешним источникам данных.</span><span class="sxs-lookup"><span data-stu-id="23972-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="23972-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23972-109">EXAMPLES</span></span>

### <span data-ttu-id="23972-110">Пример 1: создание учетных данных для каталога с указанием узла и порта</span><span class="sxs-lookup"><span data-stu-id="23972-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="23972-111">Эта команда создает указанные учетные данные для указанной учетной записи, базы данных, узла и порта по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="23972-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="23972-112">Пример 2: создание учетных данных для каталога с указанием полного URI</span><span class="sxs-lookup"><span data-stu-id="23972-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="23972-113">Эта команда создает указанные учетные данные для указанной учетной записи, идентификатора URI базы данных и внешнего источника данных.</span><span class="sxs-lookup"><span data-stu-id="23972-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="23972-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23972-114">PARAMETERS</span></span>

### <span data-ttu-id="23972-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="23972-115">-Account</span></span>
<span data-ttu-id="23972-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23972-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="23972-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="23972-117">-Credential</span></span>
<span data-ttu-id="23972-118">Указывает имя пользователя и соответствующий пароль учетных данных.</span><span class="sxs-lookup"><span data-stu-id="23972-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="23972-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="23972-119">-CredentialName</span></span>
<span data-ttu-id="23972-120">Задает имя и пароль для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="23972-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="23972-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="23972-121">-DatabaseHost</span></span>
<span data-ttu-id="23972-122">Указывает имя узла внешнего источника данных, к которому могут подключаться учетные данные в формате mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="23972-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23972-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23972-123">-DatabaseName</span></span>
<span data-ttu-id="23972-124">Указывает имя базы данных в Data Lake Analytics acocunt, в которой будут храниться учетные данные.</span><span class="sxs-lookup"><span data-stu-id="23972-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

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

### <span data-ttu-id="23972-125">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="23972-125">-Port</span></span>
<span data-ttu-id="23972-126">Указывает номер порта, который используется для подключения к указанному DatabaseHost с использованием этих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="23972-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23972-127">-URI</span><span class="sxs-lookup"><span data-stu-id="23972-127">-Uri</span></span>
<span data-ttu-id="23972-128">Указывает полный универсальный код ресурса (URI) внешнего источника данных, к которому могут подключаться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="23972-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23972-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23972-129">-Confirm</span></span>
<span data-ttu-id="23972-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23972-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23972-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23972-131">-WhatIf</span></span>
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

### <span data-ttu-id="23972-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23972-132">-DefaultProfile</span></span>
<span data-ttu-id="23972-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23972-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23972-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23972-134">CommonParameters</span></span>
<span data-ttu-id="23972-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23972-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23972-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23972-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23972-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23972-137">INPUTS</span></span>

## <span data-ttu-id="23972-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23972-138">OUTPUTS</span></span>

### <span data-ttu-id="23972-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="23972-139">None</span></span>

## <span data-ttu-id="23972-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="23972-140">NOTES</span></span>

## <span data-ttu-id="23972-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23972-141">RELATED LINKS</span></span>


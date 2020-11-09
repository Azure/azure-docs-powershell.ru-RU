---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313574"
---
# <span data-ttu-id="1dd11-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="1dd11-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="1dd11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1dd11-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd11-103">Создание учетных данных нового каталога данных Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1dd11-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="1dd11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1dd11-104">SYNTAX</span></span>

### <span data-ttu-id="1dd11-105">CreateByHostNameAndPort (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1dd11-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd11-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="1dd11-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd11-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dd11-107">DESCRIPTION</span></span>
<span data-ttu-id="1dd11-108">Командлет New-AzDataLakeAnalyticsCatalogCredential создает новые учетные данные для использования в каталоге Azure Data Lake Analytics для подключения к внешним источникам данных.</span><span class="sxs-lookup"><span data-stu-id="1dd11-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="1dd11-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1dd11-109">EXAMPLES</span></span>

### <span data-ttu-id="1dd11-110">Пример 1: создание учетных данных для каталога с указанием узла и порта</span><span class="sxs-lookup"><span data-stu-id="1dd11-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="1dd11-111">Эта команда создает указанные учетные данные для указанной учетной записи, базы данных, узла и порта по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1dd11-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="1dd11-112">Пример 2: создание учетных данных для каталога с указанием полного URI</span><span class="sxs-lookup"><span data-stu-id="1dd11-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="1dd11-113">Эта команда создает указанные учетные данные для указанной учетной записи, идентификатора URI базы данных и внешнего источника данных.</span><span class="sxs-lookup"><span data-stu-id="1dd11-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="1dd11-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1dd11-114">PARAMETERS</span></span>

### <span data-ttu-id="1dd11-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="1dd11-115">-Account</span></span>
<span data-ttu-id="1dd11-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1dd11-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1dd11-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="1dd11-117">-Credential</span></span>
<span data-ttu-id="1dd11-118">Указывает имя пользователя и соответствующий пароль учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1dd11-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="1dd11-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="1dd11-119">-CredentialName</span></span>
<span data-ttu-id="1dd11-120">Задает имя и пароль для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1dd11-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="1dd11-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="1dd11-121">-DatabaseHost</span></span>
<span data-ttu-id="1dd11-122">Указывает имя узла внешнего источника данных, к которому могут подключаться учетные данные в формате mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="1dd11-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="1dd11-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1dd11-123">-DatabaseName</span></span>
<span data-ttu-id="1dd11-124">Указывает имя базы данных в учетной записи Data Lake Analytics, в которой будут храниться учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1dd11-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="1dd11-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd11-125">-DefaultProfile</span></span>
<span data-ttu-id="1dd11-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1dd11-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dd11-127">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="1dd11-127">-Port</span></span>
<span data-ttu-id="1dd11-128">Указывает номер порта, который используется для подключения к указанному DatabaseHost с использованием этих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1dd11-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="1dd11-129">-URI</span><span class="sxs-lookup"><span data-stu-id="1dd11-129">-Uri</span></span>
<span data-ttu-id="1dd11-130">Указывает полный универсальный код ресурса (URI) внешнего источника данных, к которому могут подключаться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1dd11-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="1dd11-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dd11-131">-Confirm</span></span>
<span data-ttu-id="1dd11-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1dd11-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd11-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd11-133">-WhatIf</span></span>
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

### <span data-ttu-id="1dd11-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd11-134">CommonParameters</span></span>
<span data-ttu-id="1dd11-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1dd11-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd11-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd11-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd11-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1dd11-137">INPUTS</span></span>

### <span data-ttu-id="1dd11-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd11-138">System.String</span></span>

### <span data-ttu-id="1dd11-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="1dd11-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="1dd11-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="1dd11-140">System.Uri</span></span>

### <span data-ttu-id="1dd11-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1dd11-141">System.Int32</span></span>

## <span data-ttu-id="1dd11-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dd11-142">OUTPUTS</span></span>

### <span data-ttu-id="1dd11-143">Microsoft. Azure. Management. данных Lake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="1dd11-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="1dd11-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="1dd11-144">NOTES</span></span>

## <span data-ttu-id="1dd11-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dd11-145">RELATED LINKS</span></span>
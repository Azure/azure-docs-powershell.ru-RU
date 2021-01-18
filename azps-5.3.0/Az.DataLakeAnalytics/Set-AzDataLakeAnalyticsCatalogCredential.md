---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518729"
---
# <span data-ttu-id="86eea-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="86eea-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="86eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86eea-102">SYNOPSIS</span></span>
<span data-ttu-id="86eea-103">Изменяет пароль учетных данных каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="86eea-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="86eea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86eea-104">SYNTAX</span></span>

### <span data-ttu-id="86eea-105">SetByHostNameAndPort (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86eea-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86eea-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="86eea-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86eea-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86eea-107">DESCRIPTION</span></span>
<span data-ttu-id="86eea-108">Новый Set-AzDataLakeAnalyticsCatalogCredential изменяет пароль учетных данных, связанный с каталогом Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="86eea-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="86eea-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86eea-109">EXAMPLES</span></span>

### <span data-ttu-id="86eea-110">Пример 1. Изменение пароля учетной записи, связанной с учетной записью</span><span class="sxs-lookup"><span data-stu-id="86eea-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="86eea-111">Эта команда задает пароль для учетных данных, заданный в NewPassword.</span><span class="sxs-lookup"><span data-stu-id="86eea-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="86eea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86eea-112">PARAMETERS</span></span>

### <span data-ttu-id="86eea-113">-Account</span><span class="sxs-lookup"><span data-stu-id="86eea-113">-Account</span></span>
<span data-ttu-id="86eea-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="86eea-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="86eea-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="86eea-115">-Credential</span></span>
<span data-ttu-id="86eea-116">Имя и текущий пароль учетных данных для изменения.</span><span class="sxs-lookup"><span data-stu-id="86eea-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86eea-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="86eea-117">-CredentialName</span></span>
<span data-ttu-id="86eea-118">Указывает имя учетных данных, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="86eea-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="86eea-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="86eea-119">-DatabaseHost</span></span>
<span data-ttu-id="86eea-120">Указывает имя внешнего источника данных, к который можно подключить учетные данные, в формате mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="86eea-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86eea-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86eea-121">-DatabaseName</span></span>
<span data-ttu-id="86eea-122">Имя базы данных в учетной записи Data Lake Analytics с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="86eea-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="86eea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86eea-123">-DefaultProfile</span></span>
<span data-ttu-id="86eea-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86eea-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86eea-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="86eea-125">-NewPassword</span></span>
<span data-ttu-id="86eea-126">Новый пароль для учетных данных</span><span class="sxs-lookup"><span data-stu-id="86eea-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="86eea-127">-Port</span><span class="sxs-lookup"><span data-stu-id="86eea-127">-Port</span></span>
<span data-ttu-id="86eea-128">Номер порта, используемый для подключения к указанному databaseHost с использованием этих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="86eea-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86eea-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="86eea-129">-Uri</span></span>
<span data-ttu-id="86eea-130">Указывает полный URI внешнего источника данных, к котором могут подключаться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="86eea-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86eea-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86eea-131">-Confirm</span></span>
<span data-ttu-id="86eea-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="86eea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86eea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86eea-133">-WhatIf</span></span>
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

### <span data-ttu-id="86eea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86eea-134">CommonParameters</span></span>
<span data-ttu-id="86eea-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86eea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86eea-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86eea-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86eea-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86eea-137">INPUTS</span></span>

### <span data-ttu-id="86eea-138">System.String</span><span class="sxs-lookup"><span data-stu-id="86eea-138">System.String</span></span>

### <span data-ttu-id="86eea-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="86eea-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="86eea-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="86eea-140">System.Uri</span></span>

### <span data-ttu-id="86eea-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="86eea-141">System.Int32</span></span>

## <span data-ttu-id="86eea-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86eea-142">OUTPUTS</span></span>

### <span data-ttu-id="86eea-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="86eea-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="86eea-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86eea-144">NOTES</span></span>

## <span data-ttu-id="86eea-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86eea-145">RELATED LINKS</span></span>

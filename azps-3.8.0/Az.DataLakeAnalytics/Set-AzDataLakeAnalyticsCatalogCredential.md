---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065007"
---
# <span data-ttu-id="5e697-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="5e697-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="5e697-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e697-102">SYNOPSIS</span></span>
<span data-ttu-id="5e697-103">Изменение пароля учетных данных в каталоге Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e697-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="5e697-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e697-104">SYNTAX</span></span>

### <span data-ttu-id="5e697-105">SetByHostNameAndPort (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e697-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e697-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="5e697-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e697-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e697-107">DESCRIPTION</span></span>
<span data-ttu-id="5e697-108">Командлет Set-AzDataLakeAnalyticsCatalogCredential изменяет пароль учетных данных, связанный с каталогом Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e697-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="5e697-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e697-109">EXAMPLES</span></span>

### <span data-ttu-id="5e697-110">Пример 1: изменение пароля учетных данных, связанного с учетной записью</span><span class="sxs-lookup"><span data-stu-id="5e697-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="5e697-111">Эта команда задает пароль учетной записи, указанный в NewPassword.</span><span class="sxs-lookup"><span data-stu-id="5e697-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="5e697-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e697-112">PARAMETERS</span></span>

### <span data-ttu-id="5e697-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5e697-113">-Account</span></span>
<span data-ttu-id="5e697-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e697-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5e697-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="5e697-115">-Credential</span></span>
<span data-ttu-id="5e697-116">Указывает имя и текущий пароль учетных данных, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5e697-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="5e697-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5e697-117">-CredentialName</span></span>
<span data-ttu-id="5e697-118">Указывает имя учетных данных, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5e697-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="5e697-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="5e697-119">-DatabaseHost</span></span>
<span data-ttu-id="5e697-120">Указывает имя узла внешнего источника данных, к которому могут подключаться учетные данные в формате mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5e697-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="5e697-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e697-121">-DatabaseName</span></span>
<span data-ttu-id="5e697-122">Указывает имя базы данных в учетной записи Data Lake Analytics, содержащей учетные данные.</span><span class="sxs-lookup"><span data-stu-id="5e697-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="5e697-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e697-123">-DefaultProfile</span></span>
<span data-ttu-id="5e697-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5e697-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e697-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="5e697-125">-NewPassword</span></span>
<span data-ttu-id="5e697-126">Указывает новый пароль для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5e697-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="5e697-127">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="5e697-127">-Port</span></span>
<span data-ttu-id="5e697-128">Указывает номер порта, который используется для подключения к указанному DatabaseHost с использованием этих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5e697-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="5e697-129">-URI</span><span class="sxs-lookup"><span data-stu-id="5e697-129">-Uri</span></span>
<span data-ttu-id="5e697-130">Указывает полный универсальный код ресурса (URI) внешнего источника данных, к которому могут подключаться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="5e697-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="5e697-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e697-131">-Confirm</span></span>
<span data-ttu-id="5e697-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e697-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e697-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e697-133">-WhatIf</span></span>
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

### <span data-ttu-id="5e697-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e697-134">CommonParameters</span></span>
<span data-ttu-id="5e697-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e697-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e697-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e697-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e697-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e697-137">INPUTS</span></span>

### <span data-ttu-id="5e697-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5e697-138">System.String</span></span>

### <span data-ttu-id="5e697-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5e697-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="5e697-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="5e697-140">System.Uri</span></span>

### <span data-ttu-id="5e697-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5e697-141">System.Int32</span></span>

## <span data-ttu-id="5e697-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e697-142">OUTPUTS</span></span>

### <span data-ttu-id="5e697-143">Microsoft. Azure. Management. данных Lake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="5e697-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="5e697-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e697-144">NOTES</span></span>

## <span data-ttu-id="5e697-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e697-145">RELATED LINKS</span></span>

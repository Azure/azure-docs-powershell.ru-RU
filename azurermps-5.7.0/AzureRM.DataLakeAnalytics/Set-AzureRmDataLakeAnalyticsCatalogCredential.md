---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 7c60e6cfca0cc045d016dd763f0b64b0ad3c6550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563592"
---
# <span data-ttu-id="3c761-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="3c761-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="3c761-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c761-102">SYNOPSIS</span></span>
<span data-ttu-id="3c761-103">Изменение пароля учетных данных в каталоге Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c761-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c761-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c761-104">SYNTAX</span></span>

### <span data-ttu-id="3c761-105">SetByHostNameAndPort (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c761-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c761-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="3c761-106">SetByFullURI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c761-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c761-107">DESCRIPTION</span></span>
<span data-ttu-id="3c761-108">Командлет Set-AzureRmDataLakeAnalyticsCatalogCredential изменяет пароль учетных данных, связанный с каталогом Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c761-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="3c761-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c761-109">EXAMPLES</span></span>

### <span data-ttu-id="3c761-110">Пример 1: изменение пароля учетных данных, связанного с учетной записью</span><span class="sxs-lookup"><span data-stu-id="3c761-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="3c761-111">Эта команда задает пароль учетной записи, указанный в NewPassword.</span><span class="sxs-lookup"><span data-stu-id="3c761-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="3c761-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c761-112">PARAMETERS</span></span>

### <span data-ttu-id="3c761-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="3c761-113">-Account</span></span>
<span data-ttu-id="3c761-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c761-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="3c761-115">-Credential</span></span>
<span data-ttu-id="3c761-116">Указывает имя и текущий пароль учетных данных, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="3c761-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="3c761-117">-CredentialName</span></span>
<span data-ttu-id="3c761-118">Указывает имя учетных данных, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="3c761-118">Specifies the name of the credential to modify</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="3c761-119">-DatabaseHost</span></span>
<span data-ttu-id="3c761-120">Указывает имя узла внешнего источника данных, к которому могут подключаться учетные данные в формате mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="3c761-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c761-121">-DatabaseName</span></span>
<span data-ttu-id="3c761-122">Указывает имя базы данных в учетной записи Data Lake Analytics, содержащей учетные данные.</span><span class="sxs-lookup"><span data-stu-id="3c761-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c761-123">-DefaultProfile</span></span>
<span data-ttu-id="3c761-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3c761-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="3c761-125">-NewPassword</span></span>
<span data-ttu-id="3c761-126">Указывает новый пароль для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="3c761-126">Specifies the new password for the credential</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-127">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="3c761-127">-Port</span></span>
<span data-ttu-id="3c761-128">Указывает номер порта, который используется для подключения к указанному DatabaseHost с использованием этих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="3c761-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullURI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-129">-URI</span><span class="sxs-lookup"><span data-stu-id="3c761-129">-Uri</span></span>
<span data-ttu-id="3c761-130">Указывает полный универсальный код ресурса (URI) внешнего источника данных, к которому могут подключаться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="3c761-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c761-131">-Confirm</span></span>
<span data-ttu-id="3c761-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c761-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c761-133">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c761-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c761-134">CommonParameters</span></span>
<span data-ttu-id="3c761-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c761-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c761-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c761-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c761-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c761-137">INPUTS</span></span>

### <span data-ttu-id="3c761-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c761-138">None</span></span>
<span data-ttu-id="3c761-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3c761-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c761-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c761-140">OUTPUTS</span></span>

### <span data-ttu-id="3c761-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c761-141">None</span></span>

## <span data-ttu-id="3c761-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c761-142">NOTES</span></span>

## <span data-ttu-id="3c761-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c761-143">RELATED LINKS</span></span>


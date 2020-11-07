---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731389"
---
# <span data-ttu-id="c79ac-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c79ac-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="c79ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c79ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c79ac-103">Создание учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="c79ac-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="c79ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c79ac-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c79ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c79ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c79ac-106">Командлет **New-AzCognitiveServicesAccount** создает учетную запись службы с указанным типом и SKU.</span><span class="sxs-lookup"><span data-stu-id="c79ac-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="c79ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c79ac-107">EXAMPLES</span></span>

### <span data-ttu-id="c79ac-108">1:</span><span class="sxs-lookup"><span data-stu-id="c79ac-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="c79ac-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c79ac-109">PARAMETERS</span></span>

### <span data-ttu-id="c79ac-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="c79ac-110">-CustomSubdomainName</span></span>
<span data-ttu-id="c79ac-111">Имя поддомена учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="c79ac-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79ac-112">-DefaultProfile</span></span>
<span data-ttu-id="c79ac-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c79ac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c79ac-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c79ac-114">-Force</span></span>
<span data-ttu-id="c79ac-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c79ac-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-116">-Location</span><span class="sxs-lookup"><span data-stu-id="c79ac-116">-Location</span></span>
<span data-ttu-id="c79ac-117">Указывает место для создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c79ac-117">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c79ac-118">-Name</span></span>
<span data-ttu-id="c79ac-119">Задает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c79ac-119">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="c79ac-121">Указывает имя группы ресурсов, для которой необходимо назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="c79ac-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="c79ac-122">Группа ресурсов должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="c79ac-122">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c79ac-123">-SkuName</span></span>
<span data-ttu-id="c79ac-124">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c79ac-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="c79ac-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c79ac-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c79ac-126">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="c79ac-126">F0 (free tier)</span></span>
- <span data-ttu-id="c79ac-127">S0</span><span class="sxs-lookup"><span data-stu-id="c79ac-127">S0</span></span>
- <span data-ttu-id="c79ac-128">Состояний</span><span class="sxs-lookup"><span data-stu-id="c79ac-128">S1</span></span>
- <span data-ttu-id="c79ac-129">S2</span><span class="sxs-lookup"><span data-stu-id="c79ac-129">S2</span></span>
- <span data-ttu-id="c79ac-130">Режима</span><span class="sxs-lookup"><span data-stu-id="c79ac-130">S3</span></span>
- <span data-ttu-id="c79ac-131">Дополнительные сведения можно найти в разделе [API службы](https://www.microsoft.com/cognitive-services/en-us/apis)для наприведения.</span><span class="sxs-lookup"><span data-stu-id="c79ac-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="c79ac-132">-Tag</span></span>
<span data-ttu-id="c79ac-133">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="c79ac-133">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-134">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="c79ac-134">-Type</span></span>
<span data-ttu-id="c79ac-135">Указывает тип создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c79ac-135">Specifies the type of account to create.</span></span> <span data-ttu-id="c79ac-136">Используйте `Get-AzCognitiveServicesAccountType` командлет для получения текущих приемлемых значений.</span><span class="sxs-lookup"><span data-stu-id="c79ac-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c79ac-137">-Confirm</span></span>
<span data-ttu-id="c79ac-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c79ac-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c79ac-139">-WhatIf</span></span>
<span data-ttu-id="c79ac-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c79ac-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c79ac-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c79ac-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79ac-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79ac-142">CommonParameters</span></span>
<span data-ttu-id="c79ac-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c79ac-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79ac-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79ac-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79ac-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c79ac-145">INPUTS</span></span>

### <span data-ttu-id="c79ac-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c79ac-146">System.String</span></span>

## <span data-ttu-id="c79ac-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c79ac-147">OUTPUTS</span></span>

### <span data-ttu-id="c79ac-148">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c79ac-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="c79ac-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="c79ac-149">NOTES</span></span>

## <span data-ttu-id="c79ac-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c79ac-150">RELATED LINKS</span></span>

[<span data-ttu-id="c79ac-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c79ac-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c79ac-152">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c79ac-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c79ac-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c79ac-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)

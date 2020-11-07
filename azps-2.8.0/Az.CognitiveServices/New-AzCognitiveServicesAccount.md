---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: d19c22ffd0be5b6ea935b832d847bb74661e3106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727542"
---
# <span data-ttu-id="12aa4-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="12aa4-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="12aa4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="12aa4-103">Создание учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="12aa4-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="12aa4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12aa4-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12aa4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="12aa4-106">Командлет **New-AzCognitiveServicesAccount** создает учетную запись службы с указанным типом и SKU.</span><span class="sxs-lookup"><span data-stu-id="12aa4-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="12aa4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="12aa4-108">1:</span><span class="sxs-lookup"><span data-stu-id="12aa4-108">1:</span></span>
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

## <span data-ttu-id="12aa4-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12aa4-109">PARAMETERS</span></span>

### <span data-ttu-id="12aa4-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="12aa4-110">-CustomSubdomainName</span></span>
<span data-ttu-id="12aa4-111">Имя поддомена учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="12aa4-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="12aa4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12aa4-112">-DefaultProfile</span></span>
<span data-ttu-id="12aa4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="12aa4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12aa4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="12aa4-114">-Force</span></span>
<span data-ttu-id="12aa4-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="12aa4-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12aa4-116">-Location</span><span class="sxs-lookup"><span data-stu-id="12aa4-116">-Location</span></span>
<span data-ttu-id="12aa4-117">Указывает место для создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="12aa4-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="12aa4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12aa4-118">-Name</span></span>
<span data-ttu-id="12aa4-119">Задает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="12aa4-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="12aa4-120">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="12aa4-120">-NetworkRuleSet</span></span>
<span data-ttu-id="12aa4-121">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, например, как обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="12aa4-121">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12aa4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12aa4-122">-ResourceGroupName</span></span>
<span data-ttu-id="12aa4-123">Указывает имя группы ресурсов, для которой необходимо назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="12aa4-123">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="12aa4-124">Группа ресурсов должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="12aa4-124">The resource group must already exist.</span></span>

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

### <span data-ttu-id="12aa4-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="12aa4-125">-SkuName</span></span>
<span data-ttu-id="12aa4-126">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="12aa4-126">Specifies the SKU for the account.</span></span>
<span data-ttu-id="12aa4-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="12aa4-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="12aa4-128">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="12aa4-128">F0 (free tier)</span></span>
- <span data-ttu-id="12aa4-129">S0</span><span class="sxs-lookup"><span data-stu-id="12aa4-129">S0</span></span>
- <span data-ttu-id="12aa4-130">Состояний</span><span class="sxs-lookup"><span data-stu-id="12aa4-130">S1</span></span>
- <span data-ttu-id="12aa4-131">S2</span><span class="sxs-lookup"><span data-stu-id="12aa4-131">S2</span></span>
- <span data-ttu-id="12aa4-132">Режима</span><span class="sxs-lookup"><span data-stu-id="12aa4-132">S3</span></span>
- <span data-ttu-id="12aa4-133">Дополнительные сведения можно найти в разделе [API службы](https://www.microsoft.com/cognitive-services/en-us/apis)для наприведения.</span><span class="sxs-lookup"><span data-stu-id="12aa4-133">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="12aa4-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="12aa4-134">-Tag</span></span>
<span data-ttu-id="12aa4-135">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="12aa4-135">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="12aa4-136">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="12aa4-136">-Type</span></span>
<span data-ttu-id="12aa4-137">Указывает тип создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="12aa4-137">Specifies the type of account to create.</span></span> <span data-ttu-id="12aa4-138">Используйте `Get-AzCognitiveServicesAccountType` командлет для получения текущих приемлемых значений.</span><span class="sxs-lookup"><span data-stu-id="12aa4-138">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="12aa4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12aa4-139">-Confirm</span></span>
<span data-ttu-id="12aa4-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12aa4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12aa4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12aa4-141">-WhatIf</span></span>
<span data-ttu-id="12aa4-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12aa4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12aa4-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12aa4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12aa4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12aa4-144">CommonParameters</span></span>
<span data-ttu-id="12aa4-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12aa4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12aa4-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12aa4-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12aa4-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12aa4-147">INPUTS</span></span>

### <span data-ttu-id="12aa4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="12aa4-148">System.String</span></span>

## <span data-ttu-id="12aa4-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12aa4-149">OUTPUTS</span></span>

### <span data-ttu-id="12aa4-150">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="12aa4-150">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="12aa4-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="12aa4-151">NOTES</span></span>

## <span data-ttu-id="12aa4-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12aa4-152">RELATED LINKS</span></span>

[<span data-ttu-id="12aa4-153">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="12aa4-153">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="12aa4-154">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="12aa4-154">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="12aa4-155">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="12aa4-155">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 57d136691d6ca0ac9bcd85f205d70cf267437b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727533"
---
# <span data-ttu-id="8ff31-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ff31-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="8ff31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ff31-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff31-103">Изменение учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8ff31-103">Modifies an account.</span></span>

## <span data-ttu-id="8ff31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ff31-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ff31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ff31-105">DESCRIPTION</span></span>
<span data-ttu-id="8ff31-106">Командлет **Set-AzCognitiveServicesAccount** изменяет SKU или теги указанной учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="8ff31-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="8ff31-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ff31-107">EXAMPLES</span></span>

### <span data-ttu-id="8ff31-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ff31-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="8ff31-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ff31-109">PARAMETERS</span></span>

### <span data-ttu-id="8ff31-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="8ff31-110">-CustomSubdomainName</span></span>
<span data-ttu-id="8ff31-111">Имя поддомена учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="8ff31-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="8ff31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff31-112">-DefaultProfile</span></span>
<span data-ttu-id="8ff31-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ff31-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ff31-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8ff31-114">-Force</span></span>
<span data-ttu-id="8ff31-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ff31-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ff31-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ff31-116">-Name</span></span>
<span data-ttu-id="8ff31-117">Указывает имя учетной записи, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="8ff31-117">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="8ff31-118">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ff31-118">-NetworkRuleSet</span></span>
<span data-ttu-id="8ff31-119">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, например, как обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="8ff31-119">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="8ff31-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff31-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ff31-121">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="8ff31-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="8ff31-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8ff31-122">-SkuName</span></span>
<span data-ttu-id="8ff31-123">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8ff31-123">Specifies the SKU for the account.</span></span>
<span data-ttu-id="8ff31-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8ff31-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ff31-125">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="8ff31-125">F0 (free tier)</span></span>
- <span data-ttu-id="8ff31-126">S0</span><span class="sxs-lookup"><span data-stu-id="8ff31-126">S0</span></span>
- <span data-ttu-id="8ff31-127">Состояний</span><span class="sxs-lookup"><span data-stu-id="8ff31-127">S1</span></span>
- <span data-ttu-id="8ff31-128">S2</span><span class="sxs-lookup"><span data-stu-id="8ff31-128">S2</span></span>
- <span data-ttu-id="8ff31-129">Режима</span><span class="sxs-lookup"><span data-stu-id="8ff31-129">S3</span></span>
- <span data-ttu-id="8ff31-130">Режим</span><span class="sxs-lookup"><span data-stu-id="8ff31-130">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff31-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="8ff31-131">-Tag</span></span>
<span data-ttu-id="8ff31-132">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="8ff31-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff31-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ff31-133">-Confirm</span></span>
<span data-ttu-id="8ff31-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ff31-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ff31-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ff31-135">-WhatIf</span></span>
<span data-ttu-id="8ff31-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ff31-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ff31-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ff31-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ff31-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff31-138">CommonParameters</span></span>
<span data-ttu-id="8ff31-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ff31-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff31-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ff31-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff31-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ff31-141">INPUTS</span></span>

### <span data-ttu-id="8ff31-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8ff31-142">System.String</span></span>

### <span data-ttu-id="8ff31-143">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="8ff31-143">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="8ff31-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ff31-144">OUTPUTS</span></span>

### <span data-ttu-id="8ff31-145">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ff31-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="8ff31-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ff31-146">NOTES</span></span>

## <span data-ttu-id="8ff31-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ff31-147">RELATED LINKS</span></span>

[<span data-ttu-id="8ff31-148">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ff31-148">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8ff31-149">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ff31-149">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8ff31-150">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ff31-150">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

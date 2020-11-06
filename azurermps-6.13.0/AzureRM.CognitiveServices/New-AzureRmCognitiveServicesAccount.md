---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563119"
---
# <span data-ttu-id="f18a0-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f18a0-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="f18a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f18a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f18a0-103">Создание учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="f18a0-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f18a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f18a0-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f18a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f18a0-105">DESCRIPTION</span></span>
<span data-ttu-id="f18a0-106">Командлет **New-AzureRmCognitiveServicesAccount** создает учетную запись службы с указанным типом и SKU.</span><span class="sxs-lookup"><span data-stu-id="f18a0-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="f18a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f18a0-107">EXAMPLES</span></span>

### <span data-ttu-id="f18a0-108">1:</span><span class="sxs-lookup"><span data-stu-id="f18a0-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="f18a0-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f18a0-109">PARAMETERS</span></span>

### <span data-ttu-id="f18a0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f18a0-110">-DefaultProfile</span></span>
<span data-ttu-id="f18a0-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f18a0-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f18a0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f18a0-112">-Force</span></span>
<span data-ttu-id="f18a0-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f18a0-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f18a0-114">-Location</span><span class="sxs-lookup"><span data-stu-id="f18a0-114">-Location</span></span>
<span data-ttu-id="f18a0-115">Указывает место для создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f18a0-115">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="f18a0-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f18a0-116">-Name</span></span>
<span data-ttu-id="f18a0-117">Задает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f18a0-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="f18a0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f18a0-118">-ResourceGroupName</span></span>
<span data-ttu-id="f18a0-119">Указывает имя группы ресурсов, для которой необходимо назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f18a0-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="f18a0-120">Группа ресурсов должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="f18a0-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="f18a0-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f18a0-121">-SkuName</span></span>
<span data-ttu-id="f18a0-122">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f18a0-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="f18a0-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f18a0-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f18a0-124">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="f18a0-124">F0 (free tier)</span></span>
- <span data-ttu-id="f18a0-125">S0</span><span class="sxs-lookup"><span data-stu-id="f18a0-125">S0</span></span>
- <span data-ttu-id="f18a0-126">Состояний</span><span class="sxs-lookup"><span data-stu-id="f18a0-126">S1</span></span>
- <span data-ttu-id="f18a0-127">S2</span><span class="sxs-lookup"><span data-stu-id="f18a0-127">S2</span></span>
- <span data-ttu-id="f18a0-128">Режима</span><span class="sxs-lookup"><span data-stu-id="f18a0-128">S3</span></span>
- <span data-ttu-id="f18a0-129">Дополнительные сведения можно найти в разделе [API службы](https://www.microsoft.com/cognitive-services/en-us/apis)для наприведения.</span><span class="sxs-lookup"><span data-stu-id="f18a0-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="f18a0-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="f18a0-130">-Tag</span></span>
<span data-ttu-id="f18a0-131">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="f18a0-131">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="f18a0-132">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f18a0-132">-Type</span></span>
<span data-ttu-id="f18a0-133">Указывает тип создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f18a0-133">Specifies the type of account to create.</span></span> <span data-ttu-id="f18a0-134">Используйте `Get-AzureRmCognitiveServicesAccountType` командлет для получения текущих приемлемых значений.</span><span class="sxs-lookup"><span data-stu-id="f18a0-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="f18a0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f18a0-135">-Confirm</span></span>
<span data-ttu-id="f18a0-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f18a0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f18a0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f18a0-137">-WhatIf</span></span>
<span data-ttu-id="f18a0-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f18a0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f18a0-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f18a0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f18a0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f18a0-140">CommonParameters</span></span>
<span data-ttu-id="f18a0-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f18a0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f18a0-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f18a0-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f18a0-143">INPUTS</span></span>

### <span data-ttu-id="f18a0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f18a0-144">System.String</span></span>

## <span data-ttu-id="f18a0-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f18a0-145">OUTPUTS</span></span>

### <span data-ttu-id="f18a0-146">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f18a0-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="f18a0-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f18a0-147">NOTES</span></span>

## <span data-ttu-id="f18a0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f18a0-148">RELATED LINKS</span></span>

[<span data-ttu-id="f18a0-149">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f18a0-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="f18a0-150">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f18a0-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="f18a0-151">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f18a0-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)

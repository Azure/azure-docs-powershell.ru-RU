---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732802"
---
# <span data-ttu-id="68535-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="68535-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="68535-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68535-102">SYNOPSIS</span></span>
<span data-ttu-id="68535-103">Изменение учетной записи.</span><span class="sxs-lookup"><span data-stu-id="68535-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68535-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68535-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68535-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68535-105">DESCRIPTION</span></span>
<span data-ttu-id="68535-106">Командлет **Set-AzureRmCognitiveServicesAccount** изменяет SKU или теги указанной учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="68535-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="68535-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68535-107">EXAMPLES</span></span>

### <span data-ttu-id="68535-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68535-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="68535-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68535-109">PARAMETERS</span></span>

### <span data-ttu-id="68535-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68535-110">-DefaultProfile</span></span>
<span data-ttu-id="68535-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="68535-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68535-112">-Force</span><span class="sxs-lookup"><span data-stu-id="68535-112">-Force</span></span>
<span data-ttu-id="68535-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="68535-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68535-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68535-114">-Name</span></span>
<span data-ttu-id="68535-115">Указывает имя учетной записи, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="68535-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="68535-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68535-116">-ResourceGroupName</span></span>
<span data-ttu-id="68535-117">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="68535-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="68535-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="68535-118">-SkuName</span></span>
<span data-ttu-id="68535-119">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="68535-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="68535-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="68535-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68535-121">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="68535-121">F0 (free tier)</span></span>
- <span data-ttu-id="68535-122">S0</span><span class="sxs-lookup"><span data-stu-id="68535-122">S0</span></span>
- <span data-ttu-id="68535-123">Состояний</span><span class="sxs-lookup"><span data-stu-id="68535-123">S1</span></span>
- <span data-ttu-id="68535-124">S2</span><span class="sxs-lookup"><span data-stu-id="68535-124">S2</span></span>
- <span data-ttu-id="68535-125">Режима</span><span class="sxs-lookup"><span data-stu-id="68535-125">S3</span></span>
- <span data-ttu-id="68535-126">Режим</span><span class="sxs-lookup"><span data-stu-id="68535-126">S4</span></span>

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

### <span data-ttu-id="68535-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="68535-127">-Tag</span></span>
<span data-ttu-id="68535-128">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="68535-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="68535-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68535-129">-Confirm</span></span>
<span data-ttu-id="68535-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68535-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68535-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68535-131">-WhatIf</span></span>
<span data-ttu-id="68535-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68535-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68535-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68535-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68535-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68535-134">CommonParameters</span></span>
<span data-ttu-id="68535-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68535-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68535-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68535-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68535-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68535-137">INPUTS</span></span>

### <span data-ttu-id="68535-138">System. String</span><span class="sxs-lookup"><span data-stu-id="68535-138">System.String</span></span>

### <span data-ttu-id="68535-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="68535-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="68535-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68535-140">OUTPUTS</span></span>

### <span data-ttu-id="68535-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="68535-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="68535-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="68535-142">NOTES</span></span>

## <span data-ttu-id="68535-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68535-143">RELATED LINKS</span></span>

[<span data-ttu-id="68535-144">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="68535-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="68535-145">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="68535-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="68535-146">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="68535-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

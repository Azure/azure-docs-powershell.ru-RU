---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560359"
---
# <span data-ttu-id="1044f-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1044f-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="1044f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1044f-102">SYNOPSIS</span></span>
<span data-ttu-id="1044f-103">Создание учетной записи служб на основе расположения.</span><span class="sxs-lookup"><span data-stu-id="1044f-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1044f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1044f-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1044f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1044f-105">DESCRIPTION</span></span>
<span data-ttu-id="1044f-106">Командлет **New-AzureRmLocationBasedServicesAccount** создает учетную запись служб на основе расположения с указанным SKU.</span><span class="sxs-lookup"><span data-stu-id="1044f-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="1044f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1044f-107">EXAMPLES</span></span>

### <span data-ttu-id="1044f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1044f-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="1044f-109">Создание новой учетной записи служб на основе расположения с именем Моя учетная запись в группе ресурсов MyResourceGroup с помощью SKU S0 и тега.</span><span class="sxs-lookup"><span data-stu-id="1044f-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="1044f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1044f-110">PARAMETERS</span></span>

### <span data-ttu-id="1044f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1044f-111">-DefaultProfile</span></span>
<span data-ttu-id="1044f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1044f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1044f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1044f-113">-Force</span></span>
<span data-ttu-id="1044f-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1044f-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1044f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1044f-115">-Name</span></span>
<span data-ttu-id="1044f-116">Имя учетной записи служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="1044f-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1044f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1044f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1044f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1044f-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1044f-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1044f-119">-SkuName</span></span>
<span data-ttu-id="1044f-120">Название SKU учетной записи служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="1044f-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="1044f-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1044f-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1044f-122">S0</span><span class="sxs-lookup"><span data-stu-id="1044f-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1044f-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="1044f-123">-Tag</span></span>
<span data-ttu-id="1044f-124">Теги учетной записи служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="1044f-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1044f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1044f-125">-Confirm</span></span>
<span data-ttu-id="1044f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1044f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1044f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1044f-127">-WhatIf</span></span>
<span data-ttu-id="1044f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1044f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1044f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1044f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1044f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1044f-130">CommonParameters</span></span>
<span data-ttu-id="1044f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1044f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1044f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1044f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1044f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1044f-133">INPUTS</span></span>

### <span data-ttu-id="1044f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1044f-134">System.String</span></span>

## <span data-ttu-id="1044f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1044f-135">OUTPUTS</span></span>

### <span data-ttu-id="1044f-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1044f-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="1044f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1044f-137">NOTES</span></span>

<span data-ttu-id="1044f-138">Создание учетной записи служб на основе расположения требует ответа на запрос подтверждения условий (см https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="1044f-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="1044f-139">Параметр-Force можно использовать для обозначения принятия условий.</span><span class="sxs-lookup"><span data-stu-id="1044f-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="1044f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1044f-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566990"
---
# <span data-ttu-id="a50fd-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a50fd-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="a50fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a50fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a50fd-103">Удаление учетной записи служб на основе расположения.</span><span class="sxs-lookup"><span data-stu-id="a50fd-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a50fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a50fd-104">SYNTAX</span></span>

### <span data-ttu-id="a50fd-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a50fd-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a50fd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a50fd-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a50fd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a50fd-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a50fd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a50fd-108">DESCRIPTION</span></span>
<span data-ttu-id="a50fd-109">Командлет **Remove-AzureRmLocationBasedServicesAccount** удаляет указанную учетную запись служб на основе расположения.</span><span class="sxs-lookup"><span data-stu-id="a50fd-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="a50fd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a50fd-110">EXAMPLES</span></span>

### <span data-ttu-id="a50fd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a50fd-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a50fd-112">Удаление учетной записи Моя учетная запись из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a50fd-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a50fd-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a50fd-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a50fd-114">Удаляет указанную учетную запись служб на основе расположения.</span><span class="sxs-lookup"><span data-stu-id="a50fd-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="a50fd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a50fd-115">PARAMETERS</span></span>

### <span data-ttu-id="a50fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a50fd-116">-DefaultProfile</span></span>
<span data-ttu-id="a50fd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a50fd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a50fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a50fd-118">-InputObject</span></span>
<span data-ttu-id="a50fd-119">Учетная запись служб на основе расположения, [полученная от Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="a50fd-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a50fd-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a50fd-120">-Name</span></span>
<span data-ttu-id="a50fd-121">Имя учетной записи служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="a50fd-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a50fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="a50fd-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a50fd-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50fd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a50fd-124">-ResourceId</span></span>
<span data-ttu-id="a50fd-125">ResourceId (учетная запись) служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="a50fd-125">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50fd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a50fd-126">-Confirm</span></span>
<span data-ttu-id="a50fd-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a50fd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a50fd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a50fd-128">-WhatIf</span></span>
<span data-ttu-id="a50fd-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a50fd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a50fd-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a50fd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a50fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a50fd-131">CommonParameters</span></span>
<span data-ttu-id="a50fd-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a50fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a50fd-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a50fd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a50fd-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a50fd-134">INPUTS</span></span>

### <span data-ttu-id="a50fd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a50fd-135">System.String</span></span>

## <span data-ttu-id="a50fd-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a50fd-136">OUTPUTS</span></span>

### <span data-ttu-id="a50fd-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="a50fd-137">System.Object</span></span>

## <span data-ttu-id="a50fd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a50fd-138">NOTES</span></span>

## <span data-ttu-id="a50fd-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a50fd-139">RELATED LINKS</span></span>

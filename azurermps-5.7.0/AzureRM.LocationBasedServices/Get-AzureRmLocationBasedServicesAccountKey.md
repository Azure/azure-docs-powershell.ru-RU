---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569004"
---
# <span data-ttu-id="31dc9-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="31dc9-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="31dc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="31dc9-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="31dc9-103">Gets the API keys for an account.</span></span> <span data-ttu-id="31dc9-104">Эти ключи являются механизмом проверки подлинности, используемым при последующих звонках на службы расположения Azure.</span><span class="sxs-lookup"><span data-stu-id="31dc9-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31dc9-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31dc9-105">SYNTAX</span></span>

### <span data-ttu-id="31dc9-106">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31dc9-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31dc9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31dc9-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31dc9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31dc9-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31dc9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31dc9-109">DESCRIPTION</span></span>
<span data-ttu-id="31dc9-110">Командлет **Get-AzureRmLocationBasedServicesAccountKey** получает ключи API для учетной записи служб, основанной на местоположении.</span><span class="sxs-lookup"><span data-stu-id="31dc9-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="31dc9-111">Учетная запись служб на основе расположения имеет два ключа API: Primary и Secondary.</span><span class="sxs-lookup"><span data-stu-id="31dc9-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="31dc9-112">Ключи обеспечивают взаимодействие с конечной точкой учетной записи служб на основе расположения.</span><span class="sxs-lookup"><span data-stu-id="31dc9-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="31dc9-113">Используйте [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) для повторного создания ключа.</span><span class="sxs-lookup"><span data-stu-id="31dc9-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="31dc9-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31dc9-114">EXAMPLES</span></span>

### <span data-ttu-id="31dc9-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31dc9-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="31dc9-116">Возвращает ключи для учетной записи с именем Моя учетная запись в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="31dc9-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="31dc9-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="31dc9-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="31dc9-118">Возвращает ключи для указанной учетной записи служб на основе расположения.</span><span class="sxs-lookup"><span data-stu-id="31dc9-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="31dc9-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31dc9-119">PARAMETERS</span></span>

### <span data-ttu-id="31dc9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31dc9-120">-DefaultProfile</span></span>
<span data-ttu-id="31dc9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31dc9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31dc9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31dc9-122">-InputObject</span></span>
<span data-ttu-id="31dc9-123">Учетная запись служб на основе расположения, [полученная от Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="31dc9-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="31dc9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31dc9-124">-Name</span></span>
<span data-ttu-id="31dc9-125">Имя учетной записи служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="31dc9-125">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="31dc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31dc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="31dc9-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31dc9-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="31dc9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31dc9-128">-ResourceId</span></span>
<span data-ttu-id="31dc9-129">ResourceId (учетная запись) служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="31dc9-129">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="31dc9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31dc9-130">CommonParameters</span></span>
<span data-ttu-id="31dc9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31dc9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31dc9-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31dc9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31dc9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31dc9-133">INPUTS</span></span>

### <span data-ttu-id="31dc9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="31dc9-134">System.String</span></span>

## <span data-ttu-id="31dc9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31dc9-135">OUTPUTS</span></span>

### <span data-ttu-id="31dc9-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="31dc9-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="31dc9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31dc9-137">CommonParameters</span></span>
<span data-ttu-id="31dc9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31dc9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31dc9-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31dc9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31dc9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="31dc9-140">NOTES</span></span>

## <span data-ttu-id="31dc9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31dc9-141">RELATED LINKS</span></span>

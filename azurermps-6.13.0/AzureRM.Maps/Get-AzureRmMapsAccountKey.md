---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565382"
---
# <span data-ttu-id="ade86-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ade86-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="ade86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ade86-102">SYNOPSIS</span></span>
<span data-ttu-id="ade86-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ade86-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="ade86-104">Эти ключи являются механизмом проверки подлинности, используемым при последующих звонках на карты Azure.</span><span class="sxs-lookup"><span data-stu-id="ade86-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ade86-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ade86-105">SYNTAX</span></span>

### <span data-ttu-id="ade86-106">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ade86-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade86-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade86-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ade86-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade86-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ade86-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade86-109">DESCRIPTION</span></span>
<span data-ttu-id="ade86-110">Командлет Get-AzureRmMapsAccountKey получает ключи API для подготовленной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="ade86-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="ade86-111">Учетная запись карт Azure имеет два ключа API: Primary и Secondary.</span><span class="sxs-lookup"><span data-stu-id="ade86-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="ade86-112">Ключи обеспечивают взаимодействие с конечной точкой учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="ade86-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="ade86-113">Для повторного создания ключа используйте New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey. md).</span><span class="sxs-lookup"><span data-stu-id="ade86-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="ade86-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ade86-114">EXAMPLES</span></span>

### <span data-ttu-id="ade86-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ade86-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="ade86-116">Возвращает ключи для учетной записи с именем Моя учетная запись в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ade86-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="ade86-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ade86-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="ade86-118">Возвращает ключи для указанной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="ade86-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="ade86-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ade86-119">PARAMETERS</span></span>

### <span data-ttu-id="ade86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade86-120">-DefaultProfile</span></span>
<span data-ttu-id="ade86-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ade86-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade86-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ade86-122">-InputObject</span></span>
<span data-ttu-id="ade86-123">Карты сопоставляются с учетной записью Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="ade86-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ade86-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ade86-124">-Name</span></span>
<span data-ttu-id="ade86-125">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="ade86-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade86-126">-ResourceGroupName</span></span>
<span data-ttu-id="ade86-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade86-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade86-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ade86-128">-ResourceId</span></span>
<span data-ttu-id="ade86-129">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="ade86-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade86-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade86-130">CommonParameters</span></span>
<span data-ttu-id="ade86-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ade86-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade86-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade86-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade86-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ade86-133">INPUTS</span></span>

### <span data-ttu-id="ade86-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ade86-134">System.String</span></span>

### <span data-ttu-id="ade86-135">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="ade86-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="ade86-136">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ade86-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ade86-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade86-137">OUTPUTS</span></span>

### <span data-ttu-id="ade86-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ade86-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="ade86-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ade86-139">NOTES</span></span>

## <span data-ttu-id="ade86-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ade86-140">RELATED LINKS</span></span>

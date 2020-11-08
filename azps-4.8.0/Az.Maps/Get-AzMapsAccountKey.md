---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079021"
---
# <span data-ttu-id="98afb-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="98afb-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="98afb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98afb-102">SYNOPSIS</span></span>
<span data-ttu-id="98afb-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98afb-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="98afb-104">Эти ключи являются механизмом проверки подлинности, используемым при последующих звонках на карты Azure.</span><span class="sxs-lookup"><span data-stu-id="98afb-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="98afb-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98afb-105">SYNTAX</span></span>

### <span data-ttu-id="98afb-106">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98afb-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98afb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98afb-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98afb-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98afb-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98afb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98afb-109">DESCRIPTION</span></span>
<span data-ttu-id="98afb-110">Командлет Get-AzMapsAccountKey получает ключи API для подготовленной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="98afb-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="98afb-111">Учетная запись карт Azure имеет два ключа API: Primary и Secondary.</span><span class="sxs-lookup"><span data-stu-id="98afb-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="98afb-112">Ключи обеспечивают взаимодействие с конечной точкой учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="98afb-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="98afb-113">Для повторного создания ключа используйте New-AzMapsAccountKey (New-AzMapsAccountKey. md).</span><span class="sxs-lookup"><span data-stu-id="98afb-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="98afb-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98afb-114">EXAMPLES</span></span>

### <span data-ttu-id="98afb-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98afb-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="98afb-116">Возвращает ключи для учетной записи с именем Моя учетная запись в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="98afb-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="98afb-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98afb-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="98afb-118">Возвращает ключи для указанной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="98afb-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="98afb-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98afb-119">PARAMETERS</span></span>

### <span data-ttu-id="98afb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98afb-120">-DefaultProfile</span></span>
<span data-ttu-id="98afb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98afb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98afb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98afb-122">-InputObject</span></span>
<span data-ttu-id="98afb-123">Карты сопоставляются с учетной записью Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="98afb-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="98afb-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98afb-124">-Name</span></span>
<span data-ttu-id="98afb-125">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="98afb-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="98afb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98afb-126">-ResourceGroupName</span></span>
<span data-ttu-id="98afb-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98afb-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="98afb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98afb-128">-ResourceId</span></span>
<span data-ttu-id="98afb-129">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="98afb-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="98afb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98afb-130">CommonParameters</span></span>
<span data-ttu-id="98afb-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98afb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98afb-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98afb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98afb-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98afb-133">INPUTS</span></span>

### <span data-ttu-id="98afb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="98afb-134">System.String</span></span>

### <span data-ttu-id="98afb-135">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="98afb-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="98afb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98afb-136">OUTPUTS</span></span>

### <span data-ttu-id="98afb-137">Microsoft. Azure. Commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="98afb-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="98afb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="98afb-138">NOTES</span></span>

## <span data-ttu-id="98afb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98afb-139">RELATED LINKS</span></span>

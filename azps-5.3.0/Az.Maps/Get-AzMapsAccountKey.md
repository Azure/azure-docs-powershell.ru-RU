---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506598"
---
# <span data-ttu-id="5b713-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="5b713-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="5b713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b713-102">SYNOPSIS</span></span>
<span data-ttu-id="5b713-103">Получает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5b713-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="5b713-104">Эти ключи являются механизмом проверки подлинности, который используется при последующих звонках на карты Azure.</span><span class="sxs-lookup"><span data-stu-id="5b713-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="5b713-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b713-105">SYNTAX</span></span>

### <span data-ttu-id="5b713-106">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b713-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b713-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b713-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b713-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b713-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b713-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b713-109">DESCRIPTION</span></span>
<span data-ttu-id="5b713-110">Этот Get-AzMapsAccountKey получает ключи API для учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="5b713-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="5b713-111">Учетная запись Azure Maps имеет два ключа API: первичный и дополнительный.</span><span class="sxs-lookup"><span data-stu-id="5b713-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="5b713-112">Эти ключи обеспечивают взаимодействие с конечной точкой учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="5b713-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="5b713-113">Повторно New-AzMapsAccountKey (New-AzMapsAccountKey.md).</span><span class="sxs-lookup"><span data-stu-id="5b713-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="5b713-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b713-114">EXAMPLES</span></span>

### <span data-ttu-id="5b713-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b713-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="5b713-116">Возвращает ключи для учетной записи MyAccount в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5b713-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="5b713-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5b713-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="5b713-118">Возвращает ключи для указанной учетной записи Карты Azure.</span><span class="sxs-lookup"><span data-stu-id="5b713-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="5b713-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b713-119">PARAMETERS</span></span>

### <span data-ttu-id="5b713-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b713-120">-DefaultProfile</span></span>
<span data-ttu-id="5b713-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b713-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b713-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b713-122">-InputObject</span></span>
<span data-ttu-id="5b713-123">"Учетная запись Карты" в канале Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="5b713-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="5b713-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5b713-124">-Name</span></span>
<span data-ttu-id="5b713-125">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="5b713-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="5b713-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b713-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b713-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b713-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="5b713-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b713-128">-ResourceId</span></span>
<span data-ttu-id="5b713-129">Карты Account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5b713-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="5b713-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b713-130">CommonParameters</span></span>
<span data-ttu-id="5b713-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b713-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b713-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b713-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b713-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b713-133">INPUTS</span></span>

### <span data-ttu-id="5b713-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5b713-134">System.String</span></span>

### <span data-ttu-id="5b713-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="5b713-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="5b713-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b713-136">OUTPUTS</span></span>

### <span data-ttu-id="5b713-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5b713-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="5b713-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b713-138">NOTES</span></span>

## <span data-ttu-id="5b713-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b713-139">RELATED LINKS</span></span>

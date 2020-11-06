---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570220"
---
# <span data-ttu-id="777a2-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="777a2-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="777a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="777a2-102">SYNOPSIS</span></span>
<span data-ttu-id="777a2-103">Получает существующий ресурс верхнего уровня профиля сети</span><span class="sxs-lookup"><span data-stu-id="777a2-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="777a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="777a2-104">SYNTAX</span></span>

### <span data-ttu-id="777a2-105">NOEXPAND (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="777a2-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="777a2-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="777a2-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="777a2-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="777a2-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="777a2-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="777a2-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="777a2-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="777a2-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="777a2-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="777a2-110">DESCRIPTION</span></span>
<span data-ttu-id="777a2-111">Командлет **Get-AzureRmNetworkProfile** извлекает существующий ресурс верхнего уровня профиля сети</span><span class="sxs-lookup"><span data-stu-id="777a2-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="777a2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="777a2-112">EXAMPLES</span></span>

### <span data-ttu-id="777a2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="777a2-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="777a2-114">В результате будет извлечен профиль NP1 в группе ресурсов Rg1</span><span class="sxs-lookup"><span data-stu-id="777a2-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="777a2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="777a2-115">PARAMETERS</span></span>

### <span data-ttu-id="777a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="777a2-116">-DefaultProfile</span></span>
<span data-ttu-id="777a2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="777a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="777a2-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="777a2-118">-ExpandResource</span></span>
<span data-ttu-id="777a2-119">Развернутая ссылка на ресурс.</span><span class="sxs-lookup"><span data-stu-id="777a2-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777a2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="777a2-120">-Name</span></span>
<span data-ttu-id="777a2-121">Имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="777a2-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="777a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="777a2-123">Имя группы ресурсов в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="777a2-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="777a2-124">-ResourceId</span></span>
<span data-ttu-id="777a2-125">Идентификатор диспетчера ресурсов Azure в сетевом профиле.</span><span class="sxs-lookup"><span data-stu-id="777a2-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777a2-126">CommonParameters</span></span>
<span data-ttu-id="777a2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="777a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777a2-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="777a2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777a2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="777a2-129">INPUTS</span></span>

### <span data-ttu-id="777a2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="777a2-130">System.String</span></span>

## <span data-ttu-id="777a2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="777a2-131">OUTPUTS</span></span>

### <span data-ttu-id="777a2-132">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="777a2-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="777a2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="777a2-133">NOTES</span></span>

## <span data-ttu-id="777a2-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="777a2-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227340"
---
# <span data-ttu-id="ebd9b-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ebd9b-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="ebd9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebd9b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd9b-103">Обновляет виртуальный маршрутизатор.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="ebd9b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ebd9b-104">SYNTAX</span></span>

### <span data-ttu-id="ebd9b-105">VirtualRouterNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebd9b-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebd9b-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebd9b-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebd9b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebd9b-107">DESCRIPTION</span></span>
<span data-ttu-id="ebd9b-108">Обновляет виртуальный маршрутизатор, чтобы включить или отключить ветвь для трафика филиала.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="ebd9b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ebd9b-109">EXAMPLES</span></span>

### <span data-ttu-id="ebd9b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebd9b-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="ebd9b-111">Обновление виртуального маршрутизатора, чтобы разрешить ветвь трафика филиала.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="ebd9b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ebd9b-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="ebd9b-113">Обновление виртуального маршрутизатора для блокировки ветви на трафик филиала.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="ebd9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebd9b-114">PARAMETERS</span></span>

### <span data-ttu-id="ebd9b-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="ebd9b-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="ebd9b-116">Пометить, чтобы разрешить ветвь-трафик для виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="ebd9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd9b-117">-DefaultProfile</span></span>
<span data-ttu-id="ebd9b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebd9b-119">-ResourceGroupName</span></span>
<span data-ttu-id="ebd9b-120">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebd9b-121">-ResourceId</span></span>
<span data-ttu-id="ebd9b-122">ResourceId виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9b-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="ebd9b-123">-RouterName</span></span>
<span data-ttu-id="ebd9b-124">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd9b-125">CommonParameters</span></span>
<span data-ttu-id="ebd9b-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebd9b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd9b-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebd9b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd9b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebd9b-128">INPUTS</span></span>

### <span data-ttu-id="ebd9b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ebd9b-129">System.String</span></span>

## <span data-ttu-id="ebd9b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ebd9b-130">OUTPUTS</span></span>

### <span data-ttu-id="ebd9b-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ebd9b-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="ebd9b-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ebd9b-132">NOTES</span></span>

## <span data-ttu-id="ebd9b-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebd9b-133">RELATED LINKS</span></span>

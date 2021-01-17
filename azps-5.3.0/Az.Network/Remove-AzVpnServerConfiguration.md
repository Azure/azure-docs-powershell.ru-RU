---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425148"
---
# <span data-ttu-id="0a2f6-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a2f6-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="0a2f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2f6-103">Удаляет существующую структуру VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="0a2f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a2f6-104">SYNTAX</span></span>

### <span data-ttu-id="0a2f6-105">ByVpnServerConfigurationName (default)</span><span class="sxs-lookup"><span data-stu-id="0a2f6-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2f6-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="0a2f6-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2f6-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2f6-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a2f6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a2f6-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2f6-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="0a2f6-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0a2f6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a2f6-110">EXAMPLES</span></span>

### <span data-ttu-id="0a2f6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a2f6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="0a2f6-112">С помощью команды выше вы удалите существующую команду VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="0a2f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a2f6-113">PARAMETERS</span></span>

### <span data-ttu-id="0a2f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2f6-114">-DefaultProfile</span></span>
<span data-ttu-id="0a2f6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a2f6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0a2f6-116">-Force</span></span>
<span data-ttu-id="0a2f6-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a2f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a2f6-118">-InputObject</span></span>
<span data-ttu-id="0a2f6-119">Объект VPNServerConfiguration, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a2f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0a2f6-120">-Name</span></span>
<span data-ttu-id="0a2f6-121">Имя VPNServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2f6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a2f6-122">-PassThru</span></span>
<span data-ttu-id="0a2f6-123">Возвращает объект, представляющий элемент, с которым выполняется данной операция.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="0a2f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a2f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a2f6-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2f6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2f6-126">-ResourceId</span></span>
<span data-ttu-id="0a2f6-127">ИД ресурса Azure для удаления VPNServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a2f6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a2f6-128">-Confirm</span></span>
<span data-ttu-id="0a2f6-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a2f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a2f6-130">-WhatIf</span></span>
<span data-ttu-id="0a2f6-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a2f6-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a2f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2f6-133">CommonParameters</span></span>
<span data-ttu-id="0a2f6-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2f6-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a2f6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2f6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a2f6-136">INPUTS</span></span>

### <span data-ttu-id="0a2f6-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a2f6-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="0a2f6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0a2f6-138">System.String</span></span>

## <span data-ttu-id="0a2f6-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a2f6-139">OUTPUTS</span></span>

### <span data-ttu-id="0a2f6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a2f6-140">System.Boolean</span></span>

## <span data-ttu-id="0a2f6-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a2f6-141">NOTES</span></span>

## <span data-ttu-id="0a2f6-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a2f6-142">RELATED LINKS</span></span>

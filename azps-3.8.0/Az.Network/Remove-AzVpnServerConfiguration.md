---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073938"
---
# <span data-ttu-id="9732c-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9732c-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="9732c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9732c-102">SYNOPSIS</span></span>
<span data-ttu-id="9732c-103">Удаление существующего VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9732c-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="9732c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9732c-104">SYNTAX</span></span>

### <span data-ttu-id="9732c-105">ByVpnServerConfigurationName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9732c-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9732c-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="9732c-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9732c-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="9732c-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9732c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9732c-108">DESCRIPTION</span></span>
<span data-ttu-id="9732c-109">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="9732c-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9732c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9732c-110">EXAMPLES</span></span>

### <span data-ttu-id="9732c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9732c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="9732c-112">Команда, описанная выше, удалит существующий VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9732c-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="9732c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9732c-113">PARAMETERS</span></span>

### <span data-ttu-id="9732c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9732c-114">-DefaultProfile</span></span>
<span data-ttu-id="9732c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9732c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9732c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9732c-116">-Force</span></span>
<span data-ttu-id="9732c-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9732c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9732c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9732c-118">-InputObject</span></span>
<span data-ttu-id="9732c-119">Объект vpnServerConfiguration, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9732c-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="9732c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9732c-120">-Name</span></span>
<span data-ttu-id="9732c-121">Имя vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9732c-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="9732c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9732c-122">-PassThru</span></span>
<span data-ttu-id="9732c-123">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="9732c-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="9732c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9732c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9732c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9732c-125">The resource group name.</span></span>

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

### <span data-ttu-id="9732c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9732c-126">-ResourceId</span></span>
<span data-ttu-id="9732c-127">Идентификатор ресурса Azure для vpnServerConfiguration, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9732c-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="9732c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9732c-128">-Confirm</span></span>
<span data-ttu-id="9732c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9732c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9732c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9732c-130">-WhatIf</span></span>
<span data-ttu-id="9732c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9732c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9732c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9732c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9732c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9732c-133">CommonParameters</span></span>
<span data-ttu-id="9732c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9732c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9732c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9732c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9732c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9732c-136">INPUTS</span></span>

### <span data-ttu-id="9732c-137">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9732c-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="9732c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9732c-138">System.String</span></span>

## <span data-ttu-id="9732c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9732c-139">OUTPUTS</span></span>

### <span data-ttu-id="9732c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9732c-140">System.Boolean</span></span>

## <span data-ttu-id="9732c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9732c-141">NOTES</span></span>

## <span data-ttu-id="9732c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9732c-142">RELATED LINKS</span></span>

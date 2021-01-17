---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395991"
---
# <span data-ttu-id="a1711-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1711-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="a1711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1711-102">SYNOPSIS</span></span>
<span data-ttu-id="a1711-103">Удалить группу безопасности устройств</span><span class="sxs-lookup"><span data-stu-id="a1711-103">Delete device security group</span></span>

## <span data-ttu-id="a1711-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1711-104">SYNTAX</span></span>

### <span data-ttu-id="a1711-105">ResourceIdLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1711-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1711-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a1711-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1711-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1711-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1711-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1711-108">DESCRIPTION</span></span>
<span data-ttu-id="a1711-109">Этот Remove-AzDeviceSecurityGroup удаляет группу безопасности устройств, определенное в решении для защиты iot.</span><span class="sxs-lookup"><span data-stu-id="a1711-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="a1711-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1711-110">EXAMPLES</span></span>

### <span data-ttu-id="a1711-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1711-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="a1711-112">Удалите группу безопасности устройств "MySecurityGroup" концентратора iot с ид ресурса "/subscriptions/XXXXXXXX-XXXXX-XXXXX-XXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="a1711-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="a1711-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1711-113">PARAMETERS</span></span>

### <span data-ttu-id="a1711-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1711-114">-DefaultProfile</span></span>
<span data-ttu-id="a1711-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1711-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1711-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="a1711-116">-HubResourceId</span></span>
<span data-ttu-id="a1711-117">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="a1711-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1711-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1711-118">-InputObject</span></span>
<span data-ttu-id="a1711-119">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="a1711-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1711-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a1711-120">-Name</span></span>
<span data-ttu-id="a1711-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1711-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1711-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1711-122">-PassThru</span></span>
<span data-ttu-id="a1711-123">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="a1711-123">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1711-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1711-124">-ResourceId</span></span>
<span data-ttu-id="a1711-125">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="a1711-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1711-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1711-126">-Confirm</span></span>
<span data-ttu-id="a1711-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a1711-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1711-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1711-128">-WhatIf</span></span>
<span data-ttu-id="a1711-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1711-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1711-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a1711-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1711-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1711-131">CommonParameters</span></span>
<span data-ttu-id="a1711-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1711-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1711-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1711-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1711-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1711-134">INPUTS</span></span>

### <span data-ttu-id="a1711-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1711-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="a1711-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a1711-136">System.String</span></span>

## <span data-ttu-id="a1711-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1711-137">OUTPUTS</span></span>

### <span data-ttu-id="a1711-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a1711-138">System.Boolean</span></span>

## <span data-ttu-id="a1711-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1711-139">NOTES</span></span>

## <span data-ttu-id="a1711-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1711-140">RELATED LINKS</span></span>

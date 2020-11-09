---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243979"
---
# <span data-ttu-id="2f0fa-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2f0fa-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="2f0fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0fa-103">Удаление группы безопасности устройства</span><span class="sxs-lookup"><span data-stu-id="2f0fa-103">Delete device security group</span></span>

## <span data-ttu-id="2f0fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f0fa-104">SYNTAX</span></span>

### <span data-ttu-id="2f0fa-105">ResourceIdLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f0fa-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f0fa-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f0fa-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f0fa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0fa-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0fa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f0fa-108">DESCRIPTION</span></span>
<span data-ttu-id="2f0fa-109">Командлет Remove-AzDeviceSecurityGroup удаляет группу безопасности устройств, определенную в решении для безопасности IOT.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="2f0fa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f0fa-110">EXAMPLES</span></span>

### <span data-ttu-id="2f0fa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f0fa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="2f0fa-112">Удаление группы безопасности устройства "MySecurityGroup" центра Интернета вещей с идентификатором ресурса "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="2f0fa-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="2f0fa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f0fa-113">PARAMETERS</span></span>

### <span data-ttu-id="2f0fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0fa-114">-DefaultProfile</span></span>
<span data-ttu-id="2f0fa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f0fa-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0fa-116">-HubResourceId</span></span>
<span data-ttu-id="2f0fa-117">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2f0fa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f0fa-118">-InputObject</span></span>
<span data-ttu-id="2f0fa-119">Объект input.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-119">Input Object.</span></span>

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

### <span data-ttu-id="2f0fa-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f0fa-120">-Name</span></span>
<span data-ttu-id="2f0fa-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-121">Resource name.</span></span>

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

### <span data-ttu-id="2f0fa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f0fa-122">-PassThru</span></span>
<span data-ttu-id="2f0fa-123">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="2f0fa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0fa-124">-ResourceId</span></span>
<span data-ttu-id="2f0fa-125">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2f0fa-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f0fa-126">-Confirm</span></span>
<span data-ttu-id="2f0fa-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0fa-128">-WhatIf</span></span>
<span data-ttu-id="2f0fa-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f0fa-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f0fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0fa-131">CommonParameters</span></span>
<span data-ttu-id="2f0fa-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f0fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0fa-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f0fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0fa-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f0fa-134">INPUTS</span></span>

### <span data-ttu-id="2f0fa-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2f0fa-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="2f0fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2f0fa-136">System.String</span></span>

## <span data-ttu-id="2f0fa-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f0fa-137">OUTPUTS</span></span>

### <span data-ttu-id="2f0fa-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f0fa-138">System.Boolean</span></span>

## <span data-ttu-id="2f0fa-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f0fa-139">NOTES</span></span>

## <span data-ttu-id="2f0fa-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f0fa-140">RELATED LINKS</span></span>
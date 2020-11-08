---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236214"
---
# <span data-ttu-id="8ee81-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="8ee81-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="8ee81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ee81-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee81-103">Установка родительского устройства для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="8ee81-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="8ee81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ee81-104">SYNTAX</span></span>

### <span data-ttu-id="8ee81-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ee81-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ee81-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ee81-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee81-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8ee81-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee81-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ee81-108">DESCRIPTION</span></span>
<span data-ttu-id="8ee81-109">Настройка родительского устройства для указанного устройства без пограничного экрана.</span><span class="sxs-lookup"><span data-stu-id="8ee81-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="8ee81-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ee81-110">EXAMPLES</span></span>

### <span data-ttu-id="8ee81-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ee81-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="8ee81-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ee81-112">PARAMETERS</span></span>

### <span data-ttu-id="8ee81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee81-113">-DefaultProfile</span></span>
<span data-ttu-id="8ee81-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee81-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8ee81-115">-DeviceId</span></span>
<span data-ttu-id="8ee81-116">Идентификатор устройства, не являющегося Edge.</span><span class="sxs-lookup"><span data-stu-id="8ee81-116">Id of non-edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee81-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ee81-117">-Force</span></span>
<span data-ttu-id="8ee81-118">Перезаписывает родительский объект устройства, не являющегося Edge.</span><span class="sxs-lookup"><span data-stu-id="8ee81-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="8ee81-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ee81-119">-InputObject</span></span>
<span data-ttu-id="8ee81-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="8ee81-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee81-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8ee81-121">-IotHubName</span></span>
<span data-ttu-id="8ee81-122">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="8ee81-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee81-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="8ee81-123">-ParentDeviceId</span></span>
<span data-ttu-id="8ee81-124">Идентификатор устройства Edge.</span><span class="sxs-lookup"><span data-stu-id="8ee81-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee81-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee81-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ee81-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8ee81-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee81-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee81-127">-ResourceId</span></span>
<span data-ttu-id="8ee81-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="8ee81-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee81-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ee81-129">-Confirm</span></span>
<span data-ttu-id="8ee81-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ee81-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee81-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee81-131">-WhatIf</span></span>
<span data-ttu-id="8ee81-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ee81-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ee81-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ee81-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee81-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee81-134">CommonParameters</span></span>
<span data-ttu-id="8ee81-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ee81-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee81-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee81-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee81-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ee81-137">INPUTS</span></span>

### <span data-ttu-id="8ee81-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8ee81-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8ee81-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8ee81-139">System.String</span></span>

## <span data-ttu-id="8ee81-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ee81-140">OUTPUTS</span></span>

### <span data-ttu-id="8ee81-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="8ee81-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="8ee81-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ee81-142">NOTES</span></span>

## <span data-ttu-id="8ee81-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ee81-143">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: b7b89f239949f6a61e3388b0f5cb794cd4ad0c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004067"
---
# <span data-ttu-id="12008-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="12008-101">Update-AzIotHub</span></span>

## <span data-ttu-id="12008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12008-102">SYNOPSIS</span></span>
<span data-ttu-id="12008-103">Обновив Центр Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="12008-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="12008-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12008-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12008-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12008-105">DESCRIPTION</span></span>
<span data-ttu-id="12008-106">Вы можете обновить свойства тегов iotHub.</span><span class="sxs-lookup"><span data-stu-id="12008-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="12008-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12008-107">EXAMPLES</span></span>

### <span data-ttu-id="12008-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12008-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="12008-109">Обновление тегов концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="12008-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="12008-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12008-110">PARAMETERS</span></span>

### <span data-ttu-id="12008-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12008-111">-DefaultProfile</span></span>
<span data-ttu-id="12008-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12008-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12008-113">-Name</span><span class="sxs-lookup"><span data-stu-id="12008-113">-Name</span></span>
<span data-ttu-id="12008-114">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="12008-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12008-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="12008-115">-Reset</span></span>
<span data-ttu-id="12008-116">Сброс тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="12008-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="12008-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12008-117">-ResourceGroupName</span></span>
<span data-ttu-id="12008-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="12008-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12008-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="12008-119">-Tag</span></span>
<span data-ttu-id="12008-120">Коллекция тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="12008-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12008-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12008-121">-Confirm</span></span>
<span data-ttu-id="12008-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12008-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12008-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12008-123">-WhatIf</span></span>
<span data-ttu-id="12008-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12008-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12008-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12008-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12008-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12008-126">CommonParameters</span></span>
<span data-ttu-id="12008-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12008-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12008-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12008-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12008-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12008-129">INPUTS</span></span>

### <span data-ttu-id="12008-130">System.String</span><span class="sxs-lookup"><span data-stu-id="12008-130">System.String</span></span>

## <span data-ttu-id="12008-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12008-131">OUTPUTS</span></span>

### <span data-ttu-id="12008-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="12008-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="12008-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12008-133">NOTES</span></span>

## <span data-ttu-id="12008-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12008-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425876"
---
# <span data-ttu-id="d1bcb-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="d1bcb-101">Update-AzIotHub</span></span>

## <span data-ttu-id="d1bcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bcb-103">Обновив Центр Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="d1bcb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1bcb-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1bcb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1bcb-105">DESCRIPTION</span></span>
<span data-ttu-id="d1bcb-106">Вы можете обновить свойства тегов iotHub.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="d1bcb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1bcb-107">EXAMPLES</span></span>

### <span data-ttu-id="d1bcb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1bcb-108">Example 1</span></span>
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

<span data-ttu-id="d1bcb-109">Обновление тегов концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="d1bcb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1bcb-110">PARAMETERS</span></span>

### <span data-ttu-id="d1bcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bcb-111">-DefaultProfile</span></span>
<span data-ttu-id="d1bcb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1bcb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d1bcb-113">-Name</span></span>
<span data-ttu-id="d1bcb-114">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="d1bcb-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d1bcb-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="d1bcb-115">-Reset</span></span>
<span data-ttu-id="d1bcb-116">Сброс тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="d1bcb-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="d1bcb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bcb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1bcb-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d1bcb-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d1bcb-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1bcb-119">-Tag</span></span>
<span data-ttu-id="d1bcb-120">Коллекция тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="d1bcb-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="d1bcb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1bcb-121">-Confirm</span></span>
<span data-ttu-id="d1bcb-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1bcb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1bcb-123">-WhatIf</span></span>
<span data-ttu-id="d1bcb-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1bcb-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1bcb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bcb-126">CommonParameters</span></span>
<span data-ttu-id="d1bcb-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bcb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bcb-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bcb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bcb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1bcb-129">INPUTS</span></span>

### <span data-ttu-id="d1bcb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d1bcb-130">System.String</span></span>

## <span data-ttu-id="d1bcb-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1bcb-131">OUTPUTS</span></span>

### <span data-ttu-id="d1bcb-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d1bcb-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d1bcb-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1bcb-133">NOTES</span></span>

## <span data-ttu-id="d1bcb-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1bcb-134">RELATED LINKS</span></span>

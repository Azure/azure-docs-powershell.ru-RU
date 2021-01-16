---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411767"
---
# <span data-ttu-id="61721-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="61721-101">Update-AzIotHub</span></span>

## <span data-ttu-id="61721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61721-102">SYNOPSIS</span></span>
<span data-ttu-id="61721-103">Обновив Центр Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="61721-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="61721-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61721-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61721-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61721-105">DESCRIPTION</span></span>
<span data-ttu-id="61721-106">Вы можете обновить свойства тегов iotHub.</span><span class="sxs-lookup"><span data-stu-id="61721-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="61721-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61721-107">EXAMPLES</span></span>

### <span data-ttu-id="61721-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61721-108">Example 1</span></span>
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

<span data-ttu-id="61721-109">Обновление тегов концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="61721-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="61721-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61721-110">PARAMETERS</span></span>

### <span data-ttu-id="61721-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61721-111">-DefaultProfile</span></span>
<span data-ttu-id="61721-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61721-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61721-113">-Name</span><span class="sxs-lookup"><span data-stu-id="61721-113">-Name</span></span>
<span data-ttu-id="61721-114">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="61721-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="61721-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="61721-115">-Reset</span></span>
<span data-ttu-id="61721-116">Сброс тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="61721-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="61721-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61721-117">-ResourceGroupName</span></span>
<span data-ttu-id="61721-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="61721-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="61721-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="61721-119">-Tag</span></span>
<span data-ttu-id="61721-120">Коллекция тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="61721-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="61721-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61721-121">-Confirm</span></span>
<span data-ttu-id="61721-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="61721-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61721-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61721-123">-WhatIf</span></span>
<span data-ttu-id="61721-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61721-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61721-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61721-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61721-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61721-126">CommonParameters</span></span>
<span data-ttu-id="61721-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61721-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61721-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61721-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61721-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61721-129">INPUTS</span></span>

### <span data-ttu-id="61721-130">System.String</span><span class="sxs-lookup"><span data-stu-id="61721-130">System.String</span></span>

## <span data-ttu-id="61721-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61721-131">OUTPUTS</span></span>

### <span data-ttu-id="61721-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="61721-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="61721-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61721-133">NOTES</span></span>

## <span data-ttu-id="61721-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61721-134">RELATED LINKS</span></span>

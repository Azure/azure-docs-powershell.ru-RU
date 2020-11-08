---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 3ba9706c452c293dea6ad6a0e23a51ccb03ada9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066360"
---
# <span data-ttu-id="fb0cc-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="fb0cc-101">Update-AzIotHub</span></span>

## <span data-ttu-id="fb0cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0cc-103">Обновите центр IoT служба Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0cc-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="fb0cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb0cc-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb0cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="fb0cc-106">Вы можете обновить свойства тегов IotHub.</span><span class="sxs-lookup"><span data-stu-id="fb0cc-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="fb0cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb0cc-107">EXAMPLES</span></span>

### <span data-ttu-id="fb0cc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb0cc-108">Example 1</span></span>
```
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="fb0cc-109">Добавьте " @tags " в тег Azure IOT центр "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="fb0cc-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="fb0cc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb0cc-110">PARAMETERS</span></span>

### <span data-ttu-id="fb0cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0cc-111">-DefaultProfile</span></span>
<span data-ttu-id="fb0cc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb0cc-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb0cc-113">-Name</span></span>
<span data-ttu-id="fb0cc-114">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="fb0cc-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fb0cc-115">-Reset (Сброс)</span><span class="sxs-lookup"><span data-stu-id="fb0cc-115">-Reset</span></span>
<span data-ttu-id="fb0cc-116">Сброс тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="fb0cc-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="fb0cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb0cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb0cc-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fb0cc-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fb0cc-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="fb0cc-119">-Tag</span></span>
<span data-ttu-id="fb0cc-120">Коллекция тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="fb0cc-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="fb0cc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb0cc-121">-Confirm</span></span>
<span data-ttu-id="fb0cc-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb0cc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb0cc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb0cc-123">-WhatIf</span></span>
<span data-ttu-id="fb0cc-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb0cc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb0cc-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb0cc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb0cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0cc-126">CommonParameters</span></span>
<span data-ttu-id="fb0cc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb0cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0cc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb0cc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0cc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb0cc-129">INPUTS</span></span>

### <span data-ttu-id="fb0cc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fb0cc-130">System.String</span></span>

## <span data-ttu-id="fb0cc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb0cc-131">OUTPUTS</span></span>

### <span data-ttu-id="fb0cc-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fb0cc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="fb0cc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb0cc-133">NOTES</span></span>

## <span data-ttu-id="fb0cc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb0cc-134">RELATED LINKS</span></span>

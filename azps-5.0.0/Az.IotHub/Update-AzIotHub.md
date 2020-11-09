---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 3ba9706c452c293dea6ad6a0e23a51ccb03ada9c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312425"
---
# <span data-ttu-id="8789c-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="8789c-101">Update-AzIotHub</span></span>

## <span data-ttu-id="8789c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8789c-102">SYNOPSIS</span></span>
<span data-ttu-id="8789c-103">Обновите центр IoT служба Azure.</span><span class="sxs-lookup"><span data-stu-id="8789c-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="8789c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8789c-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8789c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8789c-105">DESCRIPTION</span></span>
<span data-ttu-id="8789c-106">Вы можете обновить свойства тегов IotHub.</span><span class="sxs-lookup"><span data-stu-id="8789c-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="8789c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8789c-107">EXAMPLES</span></span>

### <span data-ttu-id="8789c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8789c-108">Example 1</span></span>
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

<span data-ttu-id="8789c-109">Добавьте " @tags " в тег Azure IOT центр "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="8789c-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="8789c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8789c-110">PARAMETERS</span></span>

### <span data-ttu-id="8789c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8789c-111">-DefaultProfile</span></span>
<span data-ttu-id="8789c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8789c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8789c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8789c-113">-Name</span></span>
<span data-ttu-id="8789c-114">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="8789c-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8789c-115">-Reset (Сброс)</span><span class="sxs-lookup"><span data-stu-id="8789c-115">-Reset</span></span>
<span data-ttu-id="8789c-116">Сброс тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="8789c-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="8789c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8789c-117">-ResourceGroupName</span></span>
<span data-ttu-id="8789c-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8789c-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8789c-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="8789c-119">-Tag</span></span>
<span data-ttu-id="8789c-120">Коллекция тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="8789c-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="8789c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8789c-121">-Confirm</span></span>
<span data-ttu-id="8789c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8789c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8789c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8789c-123">-WhatIf</span></span>
<span data-ttu-id="8789c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8789c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8789c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8789c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8789c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8789c-126">CommonParameters</span></span>
<span data-ttu-id="8789c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8789c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8789c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8789c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8789c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8789c-129">INPUTS</span></span>

### <span data-ttu-id="8789c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8789c-130">System.String</span></span>

## <span data-ttu-id="8789c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8789c-131">OUTPUTS</span></span>

### <span data-ttu-id="8789c-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8789c-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="8789c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8789c-133">NOTES</span></span>

## <span data-ttu-id="8789c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8789c-134">RELATED LINKS</span></span>

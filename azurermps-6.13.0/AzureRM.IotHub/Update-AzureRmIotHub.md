---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/update-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
ms.openlocfilehash: 6a71c2318a709eb8d4b3fe2fe68a760919097aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568524"
---
# <span data-ttu-id="63bda-101">Update-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="63bda-101">Update-AzureRmIotHub</span></span>

## <span data-ttu-id="63bda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63bda-102">SYNOPSIS</span></span>
<span data-ttu-id="63bda-103">Обновите центр IoT служба Azure.</span><span class="sxs-lookup"><span data-stu-id="63bda-103">Update an Azure IoT Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63bda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63bda-104">SYNTAX</span></span>

```
Update-AzureRmIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63bda-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63bda-105">DESCRIPTION</span></span>
<span data-ttu-id="63bda-106">Вы можете обновить свойства тегов IotHub.</span><span class="sxs-lookup"><span data-stu-id="63bda-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="63bda-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63bda-107">EXAMPLES</span></span>

### <span data-ttu-id="63bda-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63bda-108">Example 1</span></span>
```
PS C:\> Update-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="63bda-109">Добавьте " @tags " в тег Azure IOT центр "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="63bda-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="63bda-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63bda-110">PARAMETERS</span></span>

### <span data-ttu-id="63bda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63bda-111">-DefaultProfile</span></span>
<span data-ttu-id="63bda-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63bda-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63bda-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63bda-113">-Name</span></span>
<span data-ttu-id="63bda-114">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="63bda-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="63bda-115">-Reset (Сброс)</span><span class="sxs-lookup"><span data-stu-id="63bda-115">-Reset</span></span>
<span data-ttu-id="63bda-116">Сброс тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="63bda-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="63bda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63bda-117">-ResourceGroupName</span></span>
<span data-ttu-id="63bda-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="63bda-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="63bda-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="63bda-119">-Tag</span></span>
<span data-ttu-id="63bda-120">Коллекция тегов IoTHub</span><span class="sxs-lookup"><span data-stu-id="63bda-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="63bda-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63bda-121">-Confirm</span></span>
<span data-ttu-id="63bda-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63bda-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63bda-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63bda-123">-WhatIf</span></span>
<span data-ttu-id="63bda-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63bda-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63bda-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63bda-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63bda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63bda-126">CommonParameters</span></span>
<span data-ttu-id="63bda-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63bda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63bda-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63bda-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63bda-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63bda-129">INPUTS</span></span>

### <span data-ttu-id="63bda-130">System. String</span><span class="sxs-lookup"><span data-stu-id="63bda-130">System.String</span></span>

## <span data-ttu-id="63bda-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63bda-131">OUTPUTS</span></span>

### <span data-ttu-id="63bda-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="63bda-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="63bda-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="63bda-133">NOTES</span></span>

## <span data-ttu-id="63bda-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63bda-134">RELATED LINKS</span></span>

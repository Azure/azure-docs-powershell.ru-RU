---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 674105b31c06d3def687bfc58f8b16be1c6b86f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564419"
---
# <span data-ttu-id="dd286-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="dd286-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="dd286-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd286-102">SYNOPSIS</span></span>
<span data-ttu-id="dd286-103">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="dd286-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd286-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd286-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd286-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd286-105">DESCRIPTION</span></span>
<span data-ttu-id="dd286-106">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="dd286-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="dd286-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd286-107">EXAMPLES</span></span>

### <span data-ttu-id="dd286-108">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="dd286-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="dd286-109">Удаляет IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="dd286-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="dd286-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd286-110">PARAMETERS</span></span>

### <span data-ttu-id="dd286-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd286-111">-DefaultProfile</span></span>
<span data-ttu-id="dd286-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd286-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd286-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd286-113">-Name</span></span>
<span data-ttu-id="dd286-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="dd286-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd286-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd286-115">-ResourceGroupName</span></span>
<span data-ttu-id="dd286-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd286-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd286-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd286-117">-Confirm</span></span>
<span data-ttu-id="dd286-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd286-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd286-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd286-119">-WhatIf</span></span>
<span data-ttu-id="dd286-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd286-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd286-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd286-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd286-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd286-122">CommonParameters</span></span>
<span data-ttu-id="dd286-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd286-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd286-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd286-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd286-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd286-125">INPUTS</span></span>

### <span data-ttu-id="dd286-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dd286-126">System.String</span></span>

## <span data-ttu-id="dd286-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd286-127">OUTPUTS</span></span>

### <span data-ttu-id="dd286-128">System. void</span><span class="sxs-lookup"><span data-stu-id="dd286-128">System.Void</span></span>

## <span data-ttu-id="dd286-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd286-129">NOTES</span></span>

## <span data-ttu-id="dd286-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd286-130">RELATED LINKS</span></span>

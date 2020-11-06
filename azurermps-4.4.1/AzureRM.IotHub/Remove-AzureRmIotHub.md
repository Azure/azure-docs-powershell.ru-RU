---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567616"
---
# <span data-ttu-id="ed2ac-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="ed2ac-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="ed2ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2ac-103">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed2ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed2ac-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed2ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2ac-106">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="ed2ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed2ac-107">EXAMPLES</span></span>

### <span data-ttu-id="ed2ac-108">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="ed2ac-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ed2ac-109">Удаляет IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ed2ac-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="ed2ac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed2ac-110">PARAMETERS</span></span>

### <span data-ttu-id="ed2ac-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed2ac-111">-Name</span></span>
<span data-ttu-id="ed2ac-112">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="ed2ac-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="ed2ac-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2ac-113">-ResourceGroupName</span></span>
<span data-ttu-id="ed2ac-114">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ed2ac-114">Resource Group Name</span></span>

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

### <span data-ttu-id="ed2ac-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed2ac-115">-Confirm</span></span>
<span data-ttu-id="ed2ac-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed2ac-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2ac-117">-WhatIf</span></span>
<span data-ttu-id="ed2ac-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed2ac-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed2ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2ac-120">-DefaultProfile</span></span>
<span data-ttu-id="ed2ac-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed2ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2ac-122">CommonParameters</span></span>
<span data-ttu-id="ed2ac-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2ac-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2ac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2ac-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed2ac-125">INPUTS</span></span>

### <span data-ttu-id="ed2ac-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ed2ac-126">System.String</span></span>

## <span data-ttu-id="ed2ac-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed2ac-127">OUTPUTS</span></span>

### <span data-ttu-id="ed2ac-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="ed2ac-128">System.Object</span></span>

## <span data-ttu-id="ed2ac-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed2ac-129">NOTES</span></span>

## <span data-ttu-id="ed2ac-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed2ac-130">RELATED LINKS</span></span>


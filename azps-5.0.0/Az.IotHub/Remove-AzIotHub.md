---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247737"
---
# <span data-ttu-id="f0e1c-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="f0e1c-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="f0e1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e1c-103">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="f0e1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0e1c-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0e1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e1c-106">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="f0e1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0e1c-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e1c-108">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="f0e1c-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f0e1c-109">Удаляет IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f0e1c-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="f0e1c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0e1c-110">PARAMETERS</span></span>

### <span data-ttu-id="f0e1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e1c-111">-DefaultProfile</span></span>
<span data-ttu-id="f0e1c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f0e1c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0e1c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0e1c-113">-Name</span></span>
<span data-ttu-id="f0e1c-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="f0e1c-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="f0e1c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e1c-115">-ResourceGroupName</span></span>
<span data-ttu-id="f0e1c-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0e1c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f0e1c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0e1c-117">-Confirm</span></span>
<span data-ttu-id="f0e1c-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0e1c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e1c-119">-WhatIf</span></span>
<span data-ttu-id="f0e1c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0e1c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0e1c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e1c-122">CommonParameters</span></span>
<span data-ttu-id="f0e1c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0e1c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e1c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e1c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e1c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0e1c-125">INPUTS</span></span>

### <span data-ttu-id="f0e1c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e1c-126">System.String</span></span>

## <span data-ttu-id="f0e1c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0e1c-127">OUTPUTS</span></span>

### <span data-ttu-id="f0e1c-128">System. void</span><span class="sxs-lookup"><span data-stu-id="f0e1c-128">System.Void</span></span>

## <span data-ttu-id="f0e1c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0e1c-129">NOTES</span></span>

## <span data-ttu-id="f0e1c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0e1c-130">RELATED LINKS</span></span>

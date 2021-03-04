---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 78478b28e42302ad3a672a0ee889f03807f3d1ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986037"
---
# <span data-ttu-id="b6ad8-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="b6ad8-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="b6ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ad8-103">Удаляет IotHub.</span><span class="sxs-lookup"><span data-stu-id="b6ad8-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="b6ad8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6ad8-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ad8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ad8-106">Удаляет IotHub.</span><span class="sxs-lookup"><span data-stu-id="b6ad8-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="b6ad8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6ad8-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ad8-108">Пример 1. Удаление iotHub</span><span class="sxs-lookup"><span data-stu-id="b6ad8-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b6ad8-109">Удаляет IotHub с именем Myiothub.</span><span class="sxs-lookup"><span data-stu-id="b6ad8-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="b6ad8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6ad8-110">PARAMETERS</span></span>

### <span data-ttu-id="b6ad8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ad8-111">-DefaultProfile</span></span>
<span data-ttu-id="b6ad8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6ad8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6ad8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b6ad8-113">-Name</span></span>
<span data-ttu-id="b6ad8-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="b6ad8-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="b6ad8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ad8-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6ad8-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b6ad8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b6ad8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6ad8-117">-Confirm</span></span>
<span data-ttu-id="b6ad8-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b6ad8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ad8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ad8-119">-WhatIf</span></span>
<span data-ttu-id="b6ad8-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6ad8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ad8-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6ad8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ad8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ad8-122">CommonParameters</span></span>
<span data-ttu-id="b6ad8-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ad8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ad8-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ad8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ad8-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6ad8-125">INPUTS</span></span>

### <span data-ttu-id="b6ad8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b6ad8-126">System.String</span></span>

## <span data-ttu-id="b6ad8-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6ad8-127">OUTPUTS</span></span>

### <span data-ttu-id="b6ad8-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="b6ad8-128">System.Void</span></span>

## <span data-ttu-id="b6ad8-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6ad8-129">NOTES</span></span>

## <span data-ttu-id="b6ad8-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6ad8-130">RELATED LINKS</span></span>

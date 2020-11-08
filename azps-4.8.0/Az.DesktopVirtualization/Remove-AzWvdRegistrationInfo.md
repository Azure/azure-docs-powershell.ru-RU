---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236730"
---
# <span data-ttu-id="c4c3b-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c4c3b-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="c4c3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c3b-103">Удалите данные регистрации виртуальных рабочих столов для Windows.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c4c3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4c3b-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4c3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c3b-106">Удалите данные регистрации виртуальных рабочих столов для Windows.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c4c3b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="c4c3b-108">Пример 1: Удаление маркера регистрации виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="c4c3b-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="c4c3b-109">Эта команда удаляет маркер регистрации виртуальных рабочих столов Windows в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="c4c3b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4c3b-110">PARAMETERS</span></span>

### <span data-ttu-id="c4c3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c3b-111">-DefaultProfile</span></span>
<span data-ttu-id="c4c3b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c3b-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c4c3b-113">-HostPoolName</span></span>
<span data-ttu-id="c4c3b-114">Имя пула узлов</span><span class="sxs-lookup"><span data-stu-id="c4c3b-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c3b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c3b-115">-ResourceGroupName</span></span>
<span data-ttu-id="c4c3b-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4c3b-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c3b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4c3b-117">-SubscriptionId</span></span>
<span data-ttu-id="c4c3b-118">Help foo 1</span><span class="sxs-lookup"><span data-stu-id="c4c3b-118">help foo 1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c3b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4c3b-119">-Confirm</span></span>
<span data-ttu-id="c4c3b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c3b-121">-WhatIf</span></span>
<span data-ttu-id="c4c3b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c3b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c3b-124">CommonParameters</span></span>
<span data-ttu-id="c4c3b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4c3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c3b-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4c3b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c3b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4c3b-127">INPUTS</span></span>

## <span data-ttu-id="c4c3b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4c3b-128">OUTPUTS</span></span>

## <span data-ttu-id="c4c3b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4c3b-129">NOTES</span></span>

<span data-ttu-id="c4c3b-130">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c4c3b-130">ALIASES</span></span>

## <span data-ttu-id="c4c3b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4c3b-131">RELATED LINKS</span></span>


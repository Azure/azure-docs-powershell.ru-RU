---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506365"
---
# <span data-ttu-id="3238f-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="3238f-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="3238f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3238f-102">SYNOPSIS</span></span>
<span data-ttu-id="3238f-103">Удалите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="3238f-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="3238f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3238f-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3238f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3238f-105">DESCRIPTION</span></span>
<span data-ttu-id="3238f-106">Удалите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="3238f-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="3238f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3238f-107">EXAMPLES</span></span>

### <span data-ttu-id="3238f-108">Пример 1. Удаление маркера регистрации виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="3238f-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="3238f-109">Эта команда удаляет маркер регистрации виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="3238f-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="3238f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3238f-110">PARAMETERS</span></span>

### <span data-ttu-id="3238f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3238f-111">-DefaultProfile</span></span>
<span data-ttu-id="3238f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3238f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3238f-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3238f-113">-HostPoolName</span></span>
<span data-ttu-id="3238f-114">Host Pool Name</span><span class="sxs-lookup"><span data-stu-id="3238f-114">Host Pool Name</span></span>

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

### <span data-ttu-id="3238f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3238f-115">-ResourceGroupName</span></span>
<span data-ttu-id="3238f-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3238f-116">Resource Group Name</span></span>

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

### <span data-ttu-id="3238f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3238f-117">-SubscriptionId</span></span>
<span data-ttu-id="3238f-118">справка для 1</span><span class="sxs-lookup"><span data-stu-id="3238f-118">help foo 1</span></span>

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

### <span data-ttu-id="3238f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3238f-119">-Confirm</span></span>
<span data-ttu-id="3238f-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3238f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3238f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3238f-121">-WhatIf</span></span>
<span data-ttu-id="3238f-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3238f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3238f-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3238f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3238f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3238f-124">CommonParameters</span></span>
<span data-ttu-id="3238f-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3238f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3238f-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3238f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3238f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3238f-127">INPUTS</span></span>

## <span data-ttu-id="3238f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3238f-128">OUTPUTS</span></span>

## <span data-ttu-id="3238f-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3238f-129">NOTES</span></span>

<span data-ttu-id="3238f-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3238f-130">ALIASES</span></span>

## <span data-ttu-id="3238f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3238f-131">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 7a213cbe8acacebc0f6e513e264432ca2ba08cf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990072"
---
# <span data-ttu-id="b6a0f-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6a0f-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="b6a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a0f-103">Удалите идентификацию текущего пользователя или основной службы Microsoft Partner Network (MPN).</span><span class="sxs-lookup"><span data-stu-id="b6a0f-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b6a0f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6a0f-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a0f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a0f-106">Удалите идентификацию текущего пользователя или основной службы Microsoft Partner Network (MPN).</span><span class="sxs-lookup"><span data-stu-id="b6a0f-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b6a0f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a0f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6a0f-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="b6a0f-109">Удаление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="b6a0f-109">Remove management partner</span></span>

## <span data-ttu-id="b6a0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6a0f-110">PARAMETERS</span></span>

### <span data-ttu-id="b6a0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a0f-111">-DefaultProfile</span></span>
<span data-ttu-id="b6a0f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a0f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a0f-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="b6a0f-113">-PartnerId</span></span>
<span data-ttu-id="b6a0f-114">Код партнера по управлению— это 6-значный номер.</span><span class="sxs-lookup"><span data-stu-id="b6a0f-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6a0f-115">-PassThru</span></span>
<span data-ttu-id="b6a0f-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b6a0f-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b6a0f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6a0f-117">-Confirm</span></span>
<span data-ttu-id="b6a0f-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b6a0f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a0f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a0f-119">-WhatIf</span></span>
<span data-ttu-id="b6a0f-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a0f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a0f-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6a0f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a0f-122">CommonParameters</span></span>
<span data-ttu-id="b6a0f-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a0f-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a0f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a0f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6a0f-125">INPUTS</span></span>

### <span data-ttu-id="b6a0f-126">Нет</span><span class="sxs-lookup"><span data-stu-id="b6a0f-126">None</span></span>

## <span data-ttu-id="b6a0f-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6a0f-127">OUTPUTS</span></span>

### <span data-ttu-id="b6a0f-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6a0f-128">System.Boolean</span></span>

## <span data-ttu-id="b6a0f-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6a0f-129">NOTES</span></span>

## <span data-ttu-id="b6a0f-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6a0f-130">RELATED LINKS</span></span>

[<span data-ttu-id="b6a0f-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6a0f-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="b6a0f-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6a0f-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="b6a0f-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6a0f-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 4ddeee0b0efbb55d98e8e14be1bc84ea83b38e6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963320"
---
# <span data-ttu-id="1c9df-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c9df-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="1c9df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9df-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9df-103">Удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="1c9df-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="1c9df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c9df-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9df-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c9df-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9df-106">Для удаления существующей группы управления API будет удаляема группа **Remove-AzApiManagementGroup.**</span><span class="sxs-lookup"><span data-stu-id="1c9df-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="1c9df-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c9df-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9df-108">Пример 1. Удаление существующей группы управления</span><span class="sxs-lookup"><span data-stu-id="1c9df-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="1c9df-109">Эта команда удаляет существующую группу управления с именем Group0001 и не выбирает у пользователя подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1c9df-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="1c9df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c9df-110">PARAMETERS</span></span>

### <span data-ttu-id="1c9df-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="1c9df-111">-Context</span></span>
<span data-ttu-id="1c9df-112">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="1c9df-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9df-113">-DefaultProfile</span></span>
<span data-ttu-id="1c9df-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c9df-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1c9df-115">-GroupId</span></span>
<span data-ttu-id="1c9df-116">Определяет идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="1c9df-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="1c9df-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c9df-117">-PassThru</span></span>
<span data-ttu-id="1c9df-118">Указывает на то, что этот $True возвращает значение, если он успешно, или значение $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1c9df-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9df-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c9df-119">-Confirm</span></span>
<span data-ttu-id="1c9df-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c9df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9df-121">-WhatIf</span></span>
<span data-ttu-id="1c9df-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c9df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c9df-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c9df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9df-124">CommonParameters</span></span>
<span data-ttu-id="1c9df-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9df-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c9df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9df-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c9df-127">INPUTS</span></span>

### <span data-ttu-id="1c9df-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1c9df-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c9df-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1c9df-129">System.String</span></span>

### <span data-ttu-id="1c9df-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1c9df-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c9df-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c9df-131">OUTPUTS</span></span>

### <span data-ttu-id="1c9df-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c9df-132">System.Boolean</span></span>

## <span data-ttu-id="1c9df-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c9df-133">NOTES</span></span>

## <span data-ttu-id="1c9df-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c9df-134">RELATED LINKS</span></span>

[<span data-ttu-id="1c9df-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c9df-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="1c9df-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c9df-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="1c9df-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c9df-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)



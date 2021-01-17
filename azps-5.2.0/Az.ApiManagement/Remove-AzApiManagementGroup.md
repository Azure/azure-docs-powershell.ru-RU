---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411567"
---
# <span data-ttu-id="4a54c-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4a54c-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="4a54c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a54c-102">SYNOPSIS</span></span>
<span data-ttu-id="4a54c-103">Удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="4a54c-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="4a54c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a54c-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a54c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a54c-105">DESCRIPTION</span></span>
<span data-ttu-id="4a54c-106">В **результате выполнения команды Remove-AzApiManagementGroup** удаляется существующая группа управления API.</span><span class="sxs-lookup"><span data-stu-id="4a54c-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="4a54c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a54c-107">EXAMPLES</span></span>

### <span data-ttu-id="4a54c-108">Пример 1. Удаление существующей группы управления</span><span class="sxs-lookup"><span data-stu-id="4a54c-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="4a54c-109">Эта команда удаляет существующую группу управления с именем Group0001 и не будет запросить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4a54c-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="4a54c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a54c-110">PARAMETERS</span></span>

### <span data-ttu-id="4a54c-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4a54c-111">-Context</span></span>
<span data-ttu-id="4a54c-112">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="4a54c-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4a54c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a54c-113">-DefaultProfile</span></span>
<span data-ttu-id="4a54c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a54c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a54c-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4a54c-115">-GroupId</span></span>
<span data-ttu-id="4a54c-116">Определяет идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="4a54c-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="4a54c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a54c-117">-PassThru</span></span>
<span data-ttu-id="4a54c-118">Указывает на то, что этот $True возвращает значение, если он успешно, или значение $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4a54c-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="4a54c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a54c-119">-Confirm</span></span>
<span data-ttu-id="4a54c-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4a54c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a54c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a54c-121">-WhatIf</span></span>
<span data-ttu-id="4a54c-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a54c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a54c-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a54c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a54c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a54c-124">CommonParameters</span></span>
<span data-ttu-id="4a54c-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a54c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a54c-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a54c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a54c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a54c-127">INPUTS</span></span>

### <span data-ttu-id="4a54c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4a54c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4a54c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4a54c-129">System.String</span></span>

### <span data-ttu-id="4a54c-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4a54c-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4a54c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a54c-131">OUTPUTS</span></span>

### <span data-ttu-id="4a54c-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a54c-132">System.Boolean</span></span>

## <span data-ttu-id="4a54c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a54c-133">NOTES</span></span>

## <span data-ttu-id="4a54c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a54c-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a54c-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4a54c-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="4a54c-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4a54c-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="4a54c-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4a54c-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)



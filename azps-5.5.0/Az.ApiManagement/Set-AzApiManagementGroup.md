---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233777"
---
# <span data-ttu-id="3db02-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3db02-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="3db02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3db02-102">SYNOPSIS</span></span>
<span data-ttu-id="3db02-103">Настраивает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="3db02-103">Configures an API management group.</span></span>

## <span data-ttu-id="3db02-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3db02-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3db02-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3db02-105">DESCRIPTION</span></span>
<span data-ttu-id="3db02-106">Для настройки группы управления API группа **Set-AzApiManagementGroup.**</span><span class="sxs-lookup"><span data-stu-id="3db02-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="3db02-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3db02-107">EXAMPLES</span></span>

### <span data-ttu-id="3db02-108">Пример 1. Настройка группы управления</span><span class="sxs-lookup"><span data-stu-id="3db02-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="3db02-109">Эта команда настраивает группу управления с именем Group0001.</span><span class="sxs-lookup"><span data-stu-id="3db02-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="3db02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3db02-110">PARAMETERS</span></span>

### <span data-ttu-id="3db02-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3db02-111">-Context</span></span>
<span data-ttu-id="3db02-112">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3db02-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3db02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db02-113">-DefaultProfile</span></span>
<span data-ttu-id="3db02-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3db02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3db02-115">-Description</span><span class="sxs-lookup"><span data-stu-id="3db02-115">-Description</span></span>
<span data-ttu-id="3db02-116">Описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="3db02-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3db02-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3db02-117">-GroupId</span></span>
<span data-ttu-id="3db02-118">Определяет идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="3db02-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="3db02-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3db02-119">-Name</span></span>
<span data-ttu-id="3db02-120">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="3db02-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3db02-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db02-121">-PassThru</span></span>
<span data-ttu-id="3db02-122">passthru</span><span class="sxs-lookup"><span data-stu-id="3db02-122">passthru</span></span>

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

### <span data-ttu-id="3db02-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3db02-123">-Confirm</span></span>
<span data-ttu-id="3db02-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db02-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db02-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db02-125">-WhatIf</span></span>
<span data-ttu-id="3db02-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db02-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3db02-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3db02-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db02-128">CommonParameters</span></span>
<span data-ttu-id="3db02-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db02-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3db02-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db02-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3db02-131">INPUTS</span></span>

### <span data-ttu-id="3db02-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3db02-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3db02-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3db02-133">System.String</span></span>

### <span data-ttu-id="3db02-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3db02-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3db02-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3db02-135">OUTPUTS</span></span>

### <span data-ttu-id="3db02-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3db02-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="3db02-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3db02-137">NOTES</span></span>

## <span data-ttu-id="3db02-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3db02-138">RELATED LINKS</span></span>

[<span data-ttu-id="3db02-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3db02-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="3db02-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3db02-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="3db02-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3db02-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)



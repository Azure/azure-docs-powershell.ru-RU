---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 263e54adc39103a704dc4ea0bd30f396b5d00fc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394964"
---
# <span data-ttu-id="b2560-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b2560-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="b2560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2560-102">SYNOPSIS</span></span>
<span data-ttu-id="b2560-103">Создание выпуска API для изменения его редакции.</span><span class="sxs-lookup"><span data-stu-id="b2560-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="b2560-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2560-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2560-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2560-105">DESCRIPTION</span></span>

<span data-ttu-id="b2560-106">Для изменения редакции API в контексте управления API создается выпуск API **New-AzApiManagementApiRelease.**</span><span class="sxs-lookup"><span data-stu-id="b2560-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="b2560-107">Выпуск используется для того, чтобы сделать версию Api текущей версией.</span><span class="sxs-lookup"><span data-stu-id="b2560-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="b2560-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2560-108">EXAMPLES</span></span>

### <span data-ttu-id="b2560-109">Пример 1. Создание выпуска API для изменения его редакции</span><span class="sxs-lookup"><span data-stu-id="b2560-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="b2560-110">Эта команда создает API-выпуск `2` `echo-api` редакции.</span><span class="sxs-lookup"><span data-stu-id="b2560-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="b2560-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2560-111">PARAMETERS</span></span>

### <span data-ttu-id="b2560-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b2560-112">-ApiId</span></span>
<span data-ttu-id="b2560-113">Идентификатор нового API.</span><span class="sxs-lookup"><span data-stu-id="b2560-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="b2560-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b2560-114">-ApiRevision</span></span>
<span data-ttu-id="b2560-115">Идентификатор для изменения Api.</span><span class="sxs-lookup"><span data-stu-id="b2560-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="b2560-116">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b2560-116">-Context</span></span>
<span data-ttu-id="b2560-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b2560-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b2560-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b2560-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2560-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2560-119">-DefaultProfile</span></span>
<span data-ttu-id="b2560-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2560-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2560-121">-Note</span><span class="sxs-lookup"><span data-stu-id="b2560-121">-Note</span></span>
<span data-ttu-id="b2560-122">Заметки о выпуске Api.</span><span class="sxs-lookup"><span data-stu-id="b2560-122">Api Release Notes.</span></span> <span data-ttu-id="b2560-123">Этот параметр необязателен.</span><span class="sxs-lookup"><span data-stu-id="b2560-123">This parameter is optional</span></span>

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

### <span data-ttu-id="b2560-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="b2560-124">-ReleaseId</span></span>
<span data-ttu-id="b2560-125">Идентификатор выпуска Api.</span><span class="sxs-lookup"><span data-stu-id="b2560-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="b2560-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b2560-126">This parameter is optional.</span></span>
<span data-ttu-id="b2560-127">Если не указан идентификатор, будет создан.</span><span class="sxs-lookup"><span data-stu-id="b2560-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="b2560-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2560-128">-Confirm</span></span>
<span data-ttu-id="b2560-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2560-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2560-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2560-130">-WhatIf</span></span>
<span data-ttu-id="b2560-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2560-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2560-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b2560-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2560-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2560-133">CommonParameters</span></span>
<span data-ttu-id="b2560-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2560-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2560-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2560-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2560-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2560-136">INPUTS</span></span>

### <span data-ttu-id="b2560-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b2560-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b2560-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b2560-138">System.String</span></span>

## <span data-ttu-id="b2560-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2560-139">OUTPUTS</span></span>

### <span data-ttu-id="b2560-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b2560-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="b2560-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2560-141">NOTES</span></span>

## <span data-ttu-id="b2560-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2560-142">RELATED LINKS</span></span>

[<span data-ttu-id="b2560-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b2560-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="b2560-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b2560-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="b2560-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b2560-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)
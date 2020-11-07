---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720117"
---
# <span data-ttu-id="b5710-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b5710-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="b5710-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5710-102">SYNOPSIS</span></span>
<span data-ttu-id="b5710-103">Создает выпустку API для редакции API.</span><span class="sxs-lookup"><span data-stu-id="b5710-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="b5710-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5710-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5710-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5710-105">DESCRIPTION</span></span>

<span data-ttu-id="b5710-106">Командлет **New-AzApiManagementApiRelease** создает освобождение API для редакции API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="b5710-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="b5710-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5710-107">EXAMPLES</span></span>

### <span data-ttu-id="b5710-108">Пример 1: создание выпуска API для редакции API</span><span class="sxs-lookup"><span data-stu-id="b5710-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="b5710-109">Эта команда создает набор API версии `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="b5710-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="b5710-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5710-110">PARAMETERS</span></span>

### <span data-ttu-id="b5710-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b5710-111">-ApiId</span></span>
<span data-ttu-id="b5710-112">Идентификатор для нового API.</span><span class="sxs-lookup"><span data-stu-id="b5710-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="b5710-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b5710-113">-ApiRevision</span></span>
<span data-ttu-id="b5710-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="b5710-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="b5710-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b5710-115">-Context</span></span>
<span data-ttu-id="b5710-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b5710-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b5710-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b5710-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b5710-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5710-118">-DefaultProfile</span></span>
<span data-ttu-id="b5710-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5710-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5710-120">-Примечание</span><span class="sxs-lookup"><span data-stu-id="b5710-120">-Note</span></span>
<span data-ttu-id="b5710-121">Заметки о выпуске API.</span><span class="sxs-lookup"><span data-stu-id="b5710-121">Api Release Notes.</span></span> <span data-ttu-id="b5710-122">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="b5710-122">This parameter is optional</span></span>

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

### <span data-ttu-id="b5710-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="b5710-123">-ReleaseId</span></span>
<span data-ttu-id="b5710-124">Идентификатор выпусков API.</span><span class="sxs-lookup"><span data-stu-id="b5710-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="b5710-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b5710-125">This parameter is optional.</span></span>
<span data-ttu-id="b5710-126">Если идентификатор не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="b5710-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="b5710-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5710-127">-Confirm</span></span>
<span data-ttu-id="b5710-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5710-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5710-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5710-129">-WhatIf</span></span>
<span data-ttu-id="b5710-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5710-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5710-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5710-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5710-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5710-132">CommonParameters</span></span>
<span data-ttu-id="b5710-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5710-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5710-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5710-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5710-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5710-135">INPUTS</span></span>

### <span data-ttu-id="b5710-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b5710-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b5710-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b5710-137">System.String</span></span>

## <span data-ttu-id="b5710-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5710-138">OUTPUTS</span></span>

### <span data-ttu-id="b5710-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b5710-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="b5710-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5710-140">NOTES</span></span>

## <span data-ttu-id="b5710-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5710-141">RELATED LINKS</span></span>

[<span data-ttu-id="b5710-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b5710-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="b5710-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b5710-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="b5710-144">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b5710-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)
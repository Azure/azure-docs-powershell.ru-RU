---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 263e54adc39103a704dc4ea0bd30f396b5d00fc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079242"
---
# <span data-ttu-id="bf482-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bf482-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="bf482-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf482-102">SYNOPSIS</span></span>
<span data-ttu-id="bf482-103">Создает выпустку API для редакции API.</span><span class="sxs-lookup"><span data-stu-id="bf482-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="bf482-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf482-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf482-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf482-105">DESCRIPTION</span></span>

<span data-ttu-id="bf482-106">Командлет **New-AzApiManagementApiRelease** создает освобождение API для редакции API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="bf482-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="bf482-107">Выпуск используется для того, чтобы сделать редакцию API текущей редакцией.</span><span class="sxs-lookup"><span data-stu-id="bf482-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="bf482-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf482-108">EXAMPLES</span></span>

### <span data-ttu-id="bf482-109">Пример 1: создание выпуска API для редакции API</span><span class="sxs-lookup"><span data-stu-id="bf482-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="bf482-110">Эта команда создает набор API версии `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="bf482-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="bf482-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf482-111">PARAMETERS</span></span>

### <span data-ttu-id="bf482-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bf482-112">-ApiId</span></span>
<span data-ttu-id="bf482-113">Идентификатор для нового API.</span><span class="sxs-lookup"><span data-stu-id="bf482-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="bf482-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bf482-114">-ApiRevision</span></span>
<span data-ttu-id="bf482-115">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="bf482-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="bf482-116">-Context</span><span class="sxs-lookup"><span data-stu-id="bf482-116">-Context</span></span>
<span data-ttu-id="bf482-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bf482-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bf482-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bf482-118">This parameter is required.</span></span>

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

### <span data-ttu-id="bf482-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf482-119">-DefaultProfile</span></span>
<span data-ttu-id="bf482-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf482-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf482-121">-Примечание</span><span class="sxs-lookup"><span data-stu-id="bf482-121">-Note</span></span>
<span data-ttu-id="bf482-122">Заметки о выпуске API.</span><span class="sxs-lookup"><span data-stu-id="bf482-122">Api Release Notes.</span></span> <span data-ttu-id="bf482-123">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="bf482-123">This parameter is optional</span></span>

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

### <span data-ttu-id="bf482-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="bf482-124">-ReleaseId</span></span>
<span data-ttu-id="bf482-125">Идентификатор выпусков API.</span><span class="sxs-lookup"><span data-stu-id="bf482-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="bf482-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="bf482-126">This parameter is optional.</span></span>
<span data-ttu-id="bf482-127">Если идентификатор не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="bf482-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="bf482-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf482-128">-Confirm</span></span>
<span data-ttu-id="bf482-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bf482-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf482-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf482-130">-WhatIf</span></span>
<span data-ttu-id="bf482-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bf482-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf482-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bf482-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf482-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf482-133">CommonParameters</span></span>
<span data-ttu-id="bf482-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf482-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf482-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf482-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf482-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf482-136">INPUTS</span></span>

### <span data-ttu-id="bf482-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bf482-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bf482-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bf482-138">System.String</span></span>

## <span data-ttu-id="bf482-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf482-139">OUTPUTS</span></span>

### <span data-ttu-id="bf482-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bf482-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="bf482-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf482-141">NOTES</span></span>

## <span data-ttu-id="bf482-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf482-142">RELATED LINKS</span></span>

[<span data-ttu-id="bf482-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bf482-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="bf482-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bf482-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="bf482-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bf482-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)
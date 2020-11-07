---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 2b8db6f5d550c91f806595c80be4beb300a95273
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728002"
---
# <span data-ttu-id="6469f-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6469f-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="6469f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6469f-102">SYNOPSIS</span></span>
<span data-ttu-id="6469f-103">Удалена определенная версия API</span><span class="sxs-lookup"><span data-stu-id="6469f-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="6469f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6469f-104">SYNTAX</span></span>

### <span data-ttu-id="6469f-105">ByApiId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6469f-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6469f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6469f-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6469f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6469f-107">DESCRIPTION</span></span>
<span data-ttu-id="6469f-108">Командлет **Remove-AzApiManagementApiRevision** Удаляет определенную редакцию API.</span><span class="sxs-lookup"><span data-stu-id="6469f-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="6469f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6469f-109">EXAMPLES</span></span>

### <span data-ttu-id="6469f-110">Пример 1: удаление редакции API</span><span class="sxs-lookup"><span data-stu-id="6469f-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="6469f-111">Эта команда удаляет `2` редакцию API `echo-api` из службы управления API.</span><span class="sxs-lookup"><span data-stu-id="6469f-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="6469f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6469f-112">PARAMETERS</span></span>

### <span data-ttu-id="6469f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6469f-113">-ApiId</span></span>
<span data-ttu-id="6469f-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="6469f-114">Identifier of the API.</span></span>
<span data-ttu-id="6469f-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6469f-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6469f-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6469f-116">-ApiRevision</span></span>
<span data-ttu-id="6469f-117">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="6469f-117">Identifier of the API Revision.</span></span> <span data-ttu-id="6469f-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6469f-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6469f-119">-Context</span><span class="sxs-lookup"><span data-stu-id="6469f-119">-Context</span></span>
<span data-ttu-id="6469f-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6469f-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6469f-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6469f-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6469f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6469f-122">-DefaultProfile</span></span>
<span data-ttu-id="6469f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6469f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6469f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6469f-124">-InputObject</span></span>
<span data-ttu-id="6469f-125">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="6469f-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="6469f-126">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6469f-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6469f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6469f-127">-PassThru</span></span>
<span data-ttu-id="6469f-128">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="6469f-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6469f-129">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6469f-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="6469f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6469f-130">-Confirm</span></span>
<span data-ttu-id="6469f-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6469f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6469f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6469f-132">-WhatIf</span></span>
<span data-ttu-id="6469f-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6469f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6469f-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6469f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6469f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6469f-135">CommonParameters</span></span>
<span data-ttu-id="6469f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6469f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6469f-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6469f-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6469f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6469f-138">INPUTS</span></span>

### <span data-ttu-id="6469f-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6469f-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6469f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6469f-140">System.String</span></span>

### <span data-ttu-id="6469f-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6469f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6469f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6469f-142">OUTPUTS</span></span>

### <span data-ttu-id="6469f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6469f-143">System.Boolean</span></span>

## <span data-ttu-id="6469f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6469f-144">NOTES</span></span>

## <span data-ttu-id="6469f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6469f-145">RELATED LINKS</span></span>

[<span data-ttu-id="6469f-146">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6469f-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="6469f-147">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6469f-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="6469f-148">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6469f-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)
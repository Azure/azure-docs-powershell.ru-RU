---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: fadd9732afe695d5c69f8a5c4838c68461f683d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079876"
---
# <span data-ttu-id="86c6b-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="86c6b-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="86c6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="86c6b-103">Удалена определенная версия API</span><span class="sxs-lookup"><span data-stu-id="86c6b-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="86c6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86c6b-104">SYNTAX</span></span>

### <span data-ttu-id="86c6b-105">ByApiId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86c6b-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c6b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="86c6b-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c6b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c6b-107">DESCRIPTION</span></span>
<span data-ttu-id="86c6b-108">Командлет **Remove-AzApiManagementApiRevision** Удаляет определенную редакцию API.</span><span class="sxs-lookup"><span data-stu-id="86c6b-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="86c6b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86c6b-109">EXAMPLES</span></span>

### <span data-ttu-id="86c6b-110">Пример 1: удаление редакции API</span><span class="sxs-lookup"><span data-stu-id="86c6b-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="86c6b-111">Эта команда удаляет `2` редакцию API `echo-api` из службы управления API.</span><span class="sxs-lookup"><span data-stu-id="86c6b-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

### <span data-ttu-id="86c6b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="86c6b-112">Example 2</span></span>

<span data-ttu-id="86c6b-113">Эта команда удаляет 2-API Echo API из службы управления API.</span><span class="sxs-lookup"><span data-stu-id="86c6b-113">This command removes the 2 revision of the API echo-api from API Management service.</span></span> <span data-ttu-id="86c6b-114">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="86c6b-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzApiManagementApiRevision -ApiId '0001' -ApiRevision 6 -Context <PsApiManagementContext>
```

## <span data-ttu-id="86c6b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86c6b-115">PARAMETERS</span></span>

### <span data-ttu-id="86c6b-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="86c6b-116">-ApiId</span></span>
<span data-ttu-id="86c6b-117">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="86c6b-117">Identifier of the API.</span></span>
<span data-ttu-id="86c6b-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="86c6b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="86c6b-119">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="86c6b-119">-ApiRevision</span></span>
<span data-ttu-id="86c6b-120">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="86c6b-120">Identifier of the API Revision.</span></span> <span data-ttu-id="86c6b-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="86c6b-121">This parameter is required.</span></span>

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

### <span data-ttu-id="86c6b-122">-Context</span><span class="sxs-lookup"><span data-stu-id="86c6b-122">-Context</span></span>
<span data-ttu-id="86c6b-123">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="86c6b-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="86c6b-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="86c6b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="86c6b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c6b-125">-DefaultProfile</span></span>
<span data-ttu-id="86c6b-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86c6b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86c6b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86c6b-127">-InputObject</span></span>
<span data-ttu-id="86c6b-128">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="86c6b-128">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="86c6b-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="86c6b-129">This parameter is required.</span></span>

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

### <span data-ttu-id="86c6b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86c6b-130">-PassThru</span></span>
<span data-ttu-id="86c6b-131">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="86c6b-131">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="86c6b-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="86c6b-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="86c6b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86c6b-133">-Confirm</span></span>
<span data-ttu-id="86c6b-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86c6b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c6b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c6b-135">-WhatIf</span></span>
<span data-ttu-id="86c6b-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86c6b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c6b-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86c6b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c6b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c6b-138">CommonParameters</span></span>
<span data-ttu-id="86c6b-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86c6b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c6b-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86c6b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c6b-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86c6b-141">INPUTS</span></span>

### <span data-ttu-id="86c6b-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="86c6b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="86c6b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="86c6b-143">System.String</span></span>

### <span data-ttu-id="86c6b-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="86c6b-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="86c6b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c6b-145">OUTPUTS</span></span>

### <span data-ttu-id="86c6b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86c6b-146">System.Boolean</span></span>

## <span data-ttu-id="86c6b-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="86c6b-147">NOTES</span></span>

## <span data-ttu-id="86c6b-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86c6b-148">RELATED LINKS</span></span>

[<span data-ttu-id="86c6b-149">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="86c6b-149">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="86c6b-150">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="86c6b-150">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="86c6b-151">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="86c6b-151">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)
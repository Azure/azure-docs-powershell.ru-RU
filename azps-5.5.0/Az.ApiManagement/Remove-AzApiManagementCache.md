---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212161"
---
# <span data-ttu-id="2e63b-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2e63b-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="2e63b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e63b-102">SYNOPSIS</span></span>
<span data-ttu-id="2e63b-103">Удаляет сущность кэша.</span><span class="sxs-lookup"><span data-stu-id="2e63b-103">Removes the cache entity.</span></span>

## <span data-ttu-id="2e63b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e63b-104">SYNTAX</span></span>

### <span data-ttu-id="2e63b-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e63b-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e63b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e63b-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e63b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e63b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e63b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e63b-108">DESCRIPTION</span></span>
<span data-ttu-id="2e63b-109">С его выполнения **удаляется** объект кэша.</span><span class="sxs-lookup"><span data-stu-id="2e63b-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="2e63b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e63b-110">EXAMPLES</span></span>

### <span data-ttu-id="2e63b-111">Пример 1. Удаление сущности Cache</span><span class="sxs-lookup"><span data-stu-id="2e63b-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="2e63b-112">Этот cmdlet удаляет кэш из `centralus` службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="2e63b-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="2e63b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e63b-113">PARAMETERS</span></span>

### <span data-ttu-id="2e63b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="2e63b-114">-CacheId</span></span>
<span data-ttu-id="2e63b-115">Идентификатор существующего кэшаId.</span><span class="sxs-lookup"><span data-stu-id="2e63b-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="2e63b-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="2e63b-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e63b-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="2e63b-117">-Context</span></span>
<span data-ttu-id="2e63b-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2e63b-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2e63b-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="2e63b-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e63b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e63b-120">-DefaultProfile</span></span>
<span data-ttu-id="2e63b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e63b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e63b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e63b-122">-InputObject</span></span>
<span data-ttu-id="2e63b-123">Экземпляр PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="2e63b-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="2e63b-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="2e63b-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e63b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e63b-125">-PassThru</span></span>
<span data-ttu-id="2e63b-126">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="2e63b-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2e63b-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2e63b-127">This parameter is optional.</span></span>
<span data-ttu-id="2e63b-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="2e63b-128">Default value is false.</span></span>

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

### <span data-ttu-id="2e63b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e63b-129">-ResourceId</span></span>
<span data-ttu-id="2e63b-130">Arm ResourceId кэша.</span><span class="sxs-lookup"><span data-stu-id="2e63b-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="2e63b-131">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="2e63b-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e63b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e63b-132">-Confirm</span></span>
<span data-ttu-id="2e63b-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e63b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e63b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e63b-134">-WhatIf</span></span>
<span data-ttu-id="2e63b-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e63b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e63b-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2e63b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e63b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e63b-137">CommonParameters</span></span>
<span data-ttu-id="2e63b-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e63b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e63b-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e63b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e63b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e63b-140">INPUTS</span></span>

### <span data-ttu-id="2e63b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e63b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e63b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2e63b-142">System.String</span></span>

### <span data-ttu-id="2e63b-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e63b-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e63b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e63b-144">OUTPUTS</span></span>

### <span data-ttu-id="2e63b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e63b-145">System.Boolean</span></span>

## <span data-ttu-id="2e63b-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e63b-146">NOTES</span></span>

## <span data-ttu-id="2e63b-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e63b-147">RELATED LINKS</span></span>

[<span data-ttu-id="2e63b-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2e63b-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="2e63b-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2e63b-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="2e63b-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2e63b-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317360"
---
# <span data-ttu-id="b085b-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b085b-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="b085b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b085b-102">SYNOPSIS</span></span>
<span data-ttu-id="b085b-103">Удаляет сущность кэша.</span><span class="sxs-lookup"><span data-stu-id="b085b-103">Removes the cache entity.</span></span>

## <span data-ttu-id="b085b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b085b-104">SYNTAX</span></span>

### <span data-ttu-id="b085b-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b085b-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b085b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b085b-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b085b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b085b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b085b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b085b-108">DESCRIPTION</span></span>
<span data-ttu-id="b085b-109">Командлет **Remove-AzApiManagementCache** удаляет сущность кэша.</span><span class="sxs-lookup"><span data-stu-id="b085b-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="b085b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b085b-110">EXAMPLES</span></span>

### <span data-ttu-id="b085b-111">Пример 1: Удаление сущности кэша</span><span class="sxs-lookup"><span data-stu-id="b085b-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="b085b-112">Этот командлет удаляет кэш `centralus` из службы управления API.</span><span class="sxs-lookup"><span data-stu-id="b085b-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="b085b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b085b-113">PARAMETERS</span></span>

### <span data-ttu-id="b085b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="b085b-114">-CacheId</span></span>
<span data-ttu-id="b085b-115">Идентификатор существующего cacheId.</span><span class="sxs-lookup"><span data-stu-id="b085b-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="b085b-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b085b-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b085b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b085b-117">-Context</span></span>
<span data-ttu-id="b085b-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b085b-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b085b-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b085b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b085b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b085b-120">-DefaultProfile</span></span>
<span data-ttu-id="b085b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b085b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b085b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b085b-122">-InputObject</span></span>
<span data-ttu-id="b085b-123">Экземпляр PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="b085b-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="b085b-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b085b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b085b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b085b-125">-PassThru</span></span>
<span data-ttu-id="b085b-126">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="b085b-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b085b-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b085b-127">This parameter is optional.</span></span>
<span data-ttu-id="b085b-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="b085b-128">Default value is false.</span></span>

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

### <span data-ttu-id="b085b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b085b-129">-ResourceId</span></span>
<span data-ttu-id="b085b-130">ИД ресурса ARM для кэша.</span><span class="sxs-lookup"><span data-stu-id="b085b-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="b085b-131">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b085b-131">This parameter is required.</span></span>

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

### <span data-ttu-id="b085b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b085b-132">-Confirm</span></span>
<span data-ttu-id="b085b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b085b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b085b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b085b-134">-WhatIf</span></span>
<span data-ttu-id="b085b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b085b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b085b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b085b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b085b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b085b-137">CommonParameters</span></span>
<span data-ttu-id="b085b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b085b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b085b-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b085b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b085b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b085b-140">INPUTS</span></span>

### <span data-ttu-id="b085b-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b085b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b085b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b085b-142">System.String</span></span>

### <span data-ttu-id="b085b-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b085b-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b085b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b085b-144">OUTPUTS</span></span>

### <span data-ttu-id="b085b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b085b-145">System.Boolean</span></span>

## <span data-ttu-id="b085b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b085b-146">NOTES</span></span>

## <span data-ttu-id="b085b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b085b-147">RELATED LINKS</span></span>

[<span data-ttu-id="b085b-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b085b-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="b085b-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b085b-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="b085b-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b085b-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)

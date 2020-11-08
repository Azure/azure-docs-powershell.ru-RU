---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249728"
---
# <span data-ttu-id="dd29f-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd29f-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="dd29f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd29f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd29f-103">Публикует изменения из ветви Git в базу данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dd29f-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="dd29f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd29f-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd29f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd29f-105">DESCRIPTION</span></span>
<span data-ttu-id="dd29f-106">Командлет **Publish-AzApiManagementTenantGitConfiguration** публикует изменения из ветви Git в базу данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dd29f-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="dd29f-107">Вы также можете проверить изменения в ветви Git без публикации.</span><span class="sxs-lookup"><span data-stu-id="dd29f-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="dd29f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd29f-108">EXAMPLES</span></span>

### <span data-ttu-id="dd29f-109">Пример 1: развертывание изменений Git</span><span class="sxs-lookup"><span data-stu-id="dd29f-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="dd29f-110">Эта команда публикует изменения из указанной ветви в базу данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dd29f-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="dd29f-111">Пример 2: Проверка изменений Git</span><span class="sxs-lookup"><span data-stu-id="dd29f-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="dd29f-112">Эта команда проверяет изменения в ветви Git в соответствии с базой данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dd29f-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="dd29f-113">Изменения не публикуются.</span><span class="sxs-lookup"><span data-stu-id="dd29f-113">It does not publish changes.</span></span>

## <span data-ttu-id="dd29f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd29f-114">PARAMETERS</span></span>

### <span data-ttu-id="dd29f-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="dd29f-115">-Branch</span></span>
<span data-ttu-id="dd29f-116">Указывает имя ветви Git, из которой этот командлет развертывает конфигурацию в базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dd29f-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="dd29f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="dd29f-117">-Context</span></span>
<span data-ttu-id="dd29f-118">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dd29f-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd29f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd29f-119">-DefaultProfile</span></span>
<span data-ttu-id="dd29f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd29f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd29f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dd29f-121">-Force</span></span>
<span data-ttu-id="dd29f-122">Указывает, что этот командлет удаляет подписку на продукты, удаленные в этом обновлении.</span><span class="sxs-lookup"><span data-stu-id="dd29f-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="dd29f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd29f-123">-PassThru</span></span>
<span data-ttu-id="dd29f-124">Указывает на то, что этот командлет возвращает объект **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="dd29f-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="dd29f-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="dd29f-125">-ValidateOnly</span></span>
<span data-ttu-id="dd29f-126">Указывает, что этот командлет проверяет изменения в указанной ветви Git.</span><span class="sxs-lookup"><span data-stu-id="dd29f-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="dd29f-127">Она не публикуется в базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dd29f-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="dd29f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd29f-128">-Confirm</span></span>
<span data-ttu-id="dd29f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd29f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd29f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd29f-130">-WhatIf</span></span>
<span data-ttu-id="dd29f-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd29f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd29f-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd29f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd29f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd29f-133">CommonParameters</span></span>
<span data-ttu-id="dd29f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd29f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd29f-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd29f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd29f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd29f-136">INPUTS</span></span>

### <span data-ttu-id="dd29f-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd29f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd29f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dd29f-138">System.String</span></span>

### <span data-ttu-id="dd29f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dd29f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd29f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd29f-140">OUTPUTS</span></span>

### <span data-ttu-id="dd29f-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="dd29f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="dd29f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd29f-142">NOTES</span></span>

## <span data-ttu-id="dd29f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd29f-143">RELATED LINKS</span></span>

[<span data-ttu-id="dd29f-144">Сохранить — AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd29f-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)



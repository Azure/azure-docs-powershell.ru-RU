---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066598"
---
# <span data-ttu-id="3ea9a-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ea9a-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="3ea9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ea9a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea9a-103">Сохраняет изменения, создавая фиксацию для текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="3ea9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ea9a-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ea9a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ea9a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea9a-106">Командлет **Save-AzApiManagementTenantGitConfiguration** сохраняет изменения, создавая фиксацию, которая включает текущий снимок конфигурации в ветвь в репозитории.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="3ea9a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ea9a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ea9a-108">Пример 1: сохранение изменений в настройке</span><span class="sxs-lookup"><span data-stu-id="3ea9a-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="3ea9a-109">Эта команда сохраняет изменения, создавая фиксацию с текущим снимком конфигурации для указанной ветви в репозитории.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="3ea9a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ea9a-110">PARAMETERS</span></span>

### <span data-ttu-id="3ea9a-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="3ea9a-111">-Branch</span></span>
<span data-ttu-id="3ea9a-112">Указывает имя ветви Git, в которой нужно зафиксировать текущий снимок конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="3ea9a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3ea9a-113">-Context</span></span>
<span data-ttu-id="3ea9a-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3ea9a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3ea9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea9a-115">-DefaultProfile</span></span>
<span data-ttu-id="3ea9a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ea9a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3ea9a-117">-Force</span></span>
<span data-ttu-id="3ea9a-118">Указывает, что этот командлет фиксирует текущую базу данных конфигурации в репозитории Git, даже если в репозитории Git есть более новые изменения, которые перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="3ea9a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ea9a-119">-PassThru</span></span>
<span data-ttu-id="3ea9a-120">Указывает на то, что этот командлет возвращает объект **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="3ea9a-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="3ea9a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ea9a-121">-Confirm</span></span>
<span data-ttu-id="3ea9a-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea9a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea9a-123">-WhatIf</span></span>
<span data-ttu-id="3ea9a-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ea9a-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea9a-126">CommonParameters</span></span>
<span data-ttu-id="3ea9a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ea9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea9a-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ea9a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea9a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ea9a-129">INPUTS</span></span>

### <span data-ttu-id="3ea9a-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ea9a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ea9a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3ea9a-131">System.String</span></span>

### <span data-ttu-id="3ea9a-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3ea9a-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3ea9a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ea9a-133">OUTPUTS</span></span>

### <span data-ttu-id="3ea9a-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="3ea9a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="3ea9a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ea9a-135">NOTES</span></span>

## <span data-ttu-id="3ea9a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ea9a-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ea9a-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ea9a-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)



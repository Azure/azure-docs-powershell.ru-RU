---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 91cd7855b832a406fdd3ce9a959135936ee3c284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568352"
---
# <span data-ttu-id="4ac3b-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ac3b-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="4ac3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ac3b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac3b-103">Сохраняет изменения, создавая фиксацию для текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ac3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ac3b-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ac3b-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac3b-106">Командлет **Save-AzureRmApiManagementTenantGitConfiguration** сохраняет изменения, создавая фиксацию, которая включает текущий снимок конфигурации в ветвь в репозитории.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="4ac3b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ac3b-107">EXAMPLES</span></span>

### <span data-ttu-id="4ac3b-108">Пример 1: сохранение изменений в настройке</span><span class="sxs-lookup"><span data-stu-id="4ac3b-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="4ac3b-109">Эта команда сохраняет изменения, создавая фиксацию с текущим снимком конфигурации для указанной ветви в репозитории.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="4ac3b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ac3b-110">PARAMETERS</span></span>

### <span data-ttu-id="4ac3b-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="4ac3b-111">-Branch</span></span>
<span data-ttu-id="4ac3b-112">Указывает имя ветви Git, в которой нужно зафиксировать текущий снимок конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="4ac3b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4ac3b-113">-Context</span></span>
<span data-ttu-id="4ac3b-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4ac3b-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4ac3b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4ac3b-115">-Force</span></span>
<span data-ttu-id="4ac3b-116">Указывает, что этот командлет фиксирует текущую базу данных конфигурации в репозитории Git, даже если в репозитории Git есть более новые изменения, которые перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-116">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="4ac3b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ac3b-117">-PassThru</span></span>
<span data-ttu-id="4ac3b-118">Указывает на то, что этот командлет возвращает объект **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="4ac3b-118">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="4ac3b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ac3b-119">-Confirm</span></span>
<span data-ttu-id="4ac3b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac3b-121">-WhatIf</span></span>
<span data-ttu-id="4ac3b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ac3b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac3b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac3b-124">-DefaultProfile</span></span>
<span data-ttu-id="4ac3b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac3b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac3b-126">CommonParameters</span></span>
<span data-ttu-id="4ac3b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac3b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac3b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac3b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ac3b-129">INPUTS</span></span>

## <span data-ttu-id="4ac3b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ac3b-130">OUTPUTS</span></span>

### <span data-ttu-id="4ac3b-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="4ac3b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="4ac3b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ac3b-132">NOTES</span></span>

## <span data-ttu-id="4ac3b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ac3b-133">RELATED LINKS</span></span>

[<span data-ttu-id="4ac3b-134">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ac3b-134">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)



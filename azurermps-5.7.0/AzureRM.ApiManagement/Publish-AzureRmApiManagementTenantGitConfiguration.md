---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563763"
---
# <span data-ttu-id="ea1a6-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea1a6-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="ea1a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1a6-103">Публикует изменения из ветви Git в базу данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea1a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea1a6-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea1a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea1a6-105">DESCRIPTION</span></span>
<span data-ttu-id="ea1a6-106">Командлет **Publish-AzureRmApiManagementTenantGitConfiguration** публикует изменения из ветви Git в базу данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="ea1a6-107">Вы также можете проверить изменения в ветви Git без публикации.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="ea1a6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea1a6-108">EXAMPLES</span></span>

### <span data-ttu-id="ea1a6-109">Пример 1: развертывание изменений Git</span><span class="sxs-lookup"><span data-stu-id="ea1a6-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="ea1a6-110">Эта команда публикует изменения из указанной ветви в базу данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="ea1a6-111">Пример 2: Проверка изменений Git</span><span class="sxs-lookup"><span data-stu-id="ea1a6-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="ea1a6-112">Эта команда проверяет изменения в ветви Git в соответствии с базой данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="ea1a6-113">Изменения не публикуются.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-113">It does not publish changes.</span></span>

## <span data-ttu-id="ea1a6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea1a6-114">PARAMETERS</span></span>

### <span data-ttu-id="ea1a6-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="ea1a6-115">-Branch</span></span>
<span data-ttu-id="ea1a6-116">Указывает имя ветви Git, из которой этот командлет развертывает конфигурацию в базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ea1a6-117">-Context</span></span>
<span data-ttu-id="ea1a6-118">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ea1a6-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1a6-119">-DefaultProfile</span></span>
<span data-ttu-id="ea1a6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ea1a6-121">-Force</span></span>
<span data-ttu-id="ea1a6-122">Указывает, что этот командлет удаляет подписку на продукты, удаленные в этом обновлении.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea1a6-123">-PassThru</span></span>
<span data-ttu-id="ea1a6-124">Указывает на то, что этот командлет возвращает объект **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="ea1a6-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ea1a6-125">-ValidateOnly</span></span>
<span data-ttu-id="ea1a6-126">Указывает, что этот командлет проверяет изменения в указанной ветви Git.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="ea1a6-127">Она не публикуется в базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-127">It does not publish to the configuration database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea1a6-128">-Confirm</span></span>
<span data-ttu-id="ea1a6-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1a6-130">-WhatIf</span></span>
<span data-ttu-id="ea1a6-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1a6-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1a6-133">CommonParameters</span></span>
<span data-ttu-id="ea1a6-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1a6-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea1a6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1a6-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea1a6-136">INPUTS</span></span>

### <span data-ttu-id="ea1a6-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="ea1a6-137">None</span></span>
<span data-ttu-id="ea1a6-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ea1a6-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea1a6-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea1a6-139">OUTPUTS</span></span>

### <span data-ttu-id="ea1a6-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="ea1a6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="ea1a6-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea1a6-141">NOTES</span></span>

## <span data-ttu-id="ea1a6-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea1a6-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea1a6-143">Сохранить — AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea1a6-143">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)



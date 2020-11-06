---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: cb7fbfe4ba4fdf09b9012ddc5be8028af0bd80c1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93570508"
---
# <span data-ttu-id="7505f-101">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7505f-101">New-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="7505f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7505f-102">SYNOPSIS</span></span>
<span data-ttu-id="7505f-103">Создает выпустку API для редакции API.</span><span class="sxs-lookup"><span data-stu-id="7505f-103">Creates an API Release of an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7505f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7505f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7505f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7505f-105">DESCRIPTION</span></span>

<span data-ttu-id="7505f-106">Командлет **New-AzureRmApiManagementApiRelease** создает освобождение API для редакции API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="7505f-106">The **New-AzureRmApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="7505f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7505f-107">EXAMPLES</span></span>

### <span data-ttu-id="7505f-108">Пример 1: создание выпуска API для редакции API</span><span class="sxs-lookup"><span data-stu-id="7505f-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


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

<span data-ttu-id="7505f-109">Эта команда создает набор API версии `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="7505f-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="7505f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7505f-110">PARAMETERS</span></span>

### <span data-ttu-id="7505f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7505f-111">-ApiId</span></span>
<span data-ttu-id="7505f-112">Идентификатор для нового API.</span><span class="sxs-lookup"><span data-stu-id="7505f-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="7505f-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7505f-113">-ApiRevision</span></span>
<span data-ttu-id="7505f-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="7505f-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="7505f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7505f-115">-Context</span></span>
<span data-ttu-id="7505f-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7505f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7505f-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7505f-117">This parameter is required.</span></span>

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

### <span data-ttu-id="7505f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7505f-118">-DefaultProfile</span></span>
<span data-ttu-id="7505f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7505f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7505f-120">-Примечание</span><span class="sxs-lookup"><span data-stu-id="7505f-120">-Note</span></span>
<span data-ttu-id="7505f-121">Заметки о выпуске API.</span><span class="sxs-lookup"><span data-stu-id="7505f-121">Api Release Notes.</span></span> <span data-ttu-id="7505f-122">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="7505f-122">This parameter is optional</span></span>

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

### <span data-ttu-id="7505f-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="7505f-123">-ReleaseId</span></span>
<span data-ttu-id="7505f-124">Идентификатор выпусков API.</span><span class="sxs-lookup"><span data-stu-id="7505f-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="7505f-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7505f-125">This parameter is optional.</span></span>
<span data-ttu-id="7505f-126">Если идентификатор не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="7505f-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="7505f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7505f-127">-Confirm</span></span>
<span data-ttu-id="7505f-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7505f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7505f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7505f-129">-WhatIf</span></span>
<span data-ttu-id="7505f-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7505f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7505f-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7505f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7505f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7505f-132">CommonParameters</span></span>
<span data-ttu-id="7505f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7505f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7505f-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7505f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7505f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7505f-135">INPUTS</span></span>

### <span data-ttu-id="7505f-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7505f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="7505f-137">Параметры: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7505f-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="7505f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7505f-138">System.String</span></span>

## <span data-ttu-id="7505f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7505f-139">OUTPUTS</span></span>

### <span data-ttu-id="7505f-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7505f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="7505f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="7505f-141">NOTES</span></span>

## <span data-ttu-id="7505f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7505f-142">RELATED LINKS</span></span>

[<span data-ttu-id="7505f-143">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7505f-143">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="7505f-144">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7505f-144">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="7505f-145">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7505f-145">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)

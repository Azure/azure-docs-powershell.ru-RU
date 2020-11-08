---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247512"
---
# <span data-ttu-id="98f2f-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98f2f-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="98f2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="98f2f-103">Создает экземпляр PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="98f2f-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="98f2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98f2f-104">SYNTAX</span></span>

### <span data-ttu-id="98f2f-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98f2f-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f2f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98f2f-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98f2f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="98f2f-108">Командлет **New-AzApiManagementContext** создает экземпляр класса **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="98f2f-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="98f2f-109">Контекст используется для всех командлетов службы управления API.</span><span class="sxs-lookup"><span data-stu-id="98f2f-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="98f2f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98f2f-110">EXAMPLES</span></span>

### <span data-ttu-id="98f2f-111">Пример 1: создание экземпляра PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98f2f-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="98f2f-112">Эта команда создает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="98f2f-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="98f2f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98f2f-113">PARAMETERS</span></span>

### <span data-ttu-id="98f2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f2f-114">-DefaultProfile</span></span>
<span data-ttu-id="98f2f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98f2f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f2f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f2f-116">-ResourceGroupName</span></span>
<span data-ttu-id="98f2f-117">Указывает имя группы ресурсов, в которой развернута служба управления API.</span><span class="sxs-lookup"><span data-stu-id="98f2f-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f2f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f2f-118">-ResourceId</span></span>
<span data-ttu-id="98f2f-119">Идентификатор ресурса ARM службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="98f2f-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="98f2f-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="98f2f-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f2f-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="98f2f-121">-ServiceName</span></span>
<span data-ttu-id="98f2f-122">Указывает имя развернутой службы управления API.</span><span class="sxs-lookup"><span data-stu-id="98f2f-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f2f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f2f-123">CommonParameters</span></span>
<span data-ttu-id="98f2f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98f2f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f2f-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98f2f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f2f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98f2f-126">INPUTS</span></span>

### <span data-ttu-id="98f2f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="98f2f-127">System.String</span></span>

## <span data-ttu-id="98f2f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f2f-128">OUTPUTS</span></span>

### <span data-ttu-id="98f2f-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98f2f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="98f2f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="98f2f-130">NOTES</span></span>

## <span data-ttu-id="98f2f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98f2f-131">RELATED LINKS</span></span>

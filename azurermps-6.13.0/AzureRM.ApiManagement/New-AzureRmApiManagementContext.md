---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 56dc320ea6aafd37e93912071a3256040342e2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567331"
---
# <span data-ttu-id="c55d3-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c55d3-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="c55d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c55d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c55d3-103">Создает экземпляр PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c55d3-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c55d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c55d3-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c55d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c55d3-105">DESCRIPTION</span></span>
<span data-ttu-id="c55d3-106">Командлет **New-AzureRmApiManagementContext** создает экземпляр класса **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="c55d3-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="c55d3-107">Контекст используется для всех командлетов службы управления API.</span><span class="sxs-lookup"><span data-stu-id="c55d3-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="c55d3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c55d3-108">EXAMPLES</span></span>

### <span data-ttu-id="c55d3-109">Пример 1: создание экземпляра PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c55d3-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="c55d3-110">Эта команда создает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="c55d3-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="c55d3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c55d3-111">PARAMETERS</span></span>

### <span data-ttu-id="c55d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55d3-112">-DefaultProfile</span></span>
<span data-ttu-id="c55d3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c55d3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c55d3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c55d3-114">-ResourceGroupName</span></span>
<span data-ttu-id="c55d3-115">Указывает имя группы ресурсов, в которой развернута служба управления API.</span><span class="sxs-lookup"><span data-stu-id="c55d3-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="c55d3-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c55d3-116">-ServiceName</span></span>
<span data-ttu-id="c55d3-117">Указывает имя развернутой службы управления API.</span><span class="sxs-lookup"><span data-stu-id="c55d3-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="c55d3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55d3-118">CommonParameters</span></span>
<span data-ttu-id="c55d3-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c55d3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55d3-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c55d3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55d3-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c55d3-121">INPUTS</span></span>

### <span data-ttu-id="c55d3-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c55d3-122">System.String</span></span>

## <span data-ttu-id="c55d3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c55d3-123">OUTPUTS</span></span>

### <span data-ttu-id="c55d3-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c55d3-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="c55d3-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="c55d3-125">NOTES</span></span>

## <span data-ttu-id="c55d3-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c55d3-126">RELATED LINKS</span></span>

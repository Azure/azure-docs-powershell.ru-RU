---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 7bf97454fd7dc4a2debc8861766981f6428f0b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565731"
---
# <span data-ttu-id="268f6-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="268f6-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="268f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="268f6-102">SYNOPSIS</span></span>
<span data-ttu-id="268f6-103">Создает экземпляр PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="268f6-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="268f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="268f6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="268f6-105">DESCRIPTION</span></span>
<span data-ttu-id="268f6-106">Командлет **New-AzureRmApiManagementContext** создает экземпляр класса **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="268f6-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="268f6-107">Контекст используется для всех командлетов службы управления API.</span><span class="sxs-lookup"><span data-stu-id="268f6-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="268f6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="268f6-108">EXAMPLES</span></span>

### <span data-ttu-id="268f6-109">Пример 1: создание экземпляра PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="268f6-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="268f6-110">Эта команда создает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="268f6-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="268f6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="268f6-111">PARAMETERS</span></span>

### <span data-ttu-id="268f6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268f6-112">-ResourceGroupName</span></span>
<span data-ttu-id="268f6-113">Указывает имя группы ресурсов, в которой развернута служба управления API.</span><span class="sxs-lookup"><span data-stu-id="268f6-113">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="268f6-114">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="268f6-114">-ServiceName</span></span>
<span data-ttu-id="268f6-115">Указывает имя развернутой службы управления API.</span><span class="sxs-lookup"><span data-stu-id="268f6-115">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="268f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268f6-116">-DefaultProfile</span></span>
<span data-ttu-id="268f6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="268f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268f6-118">CommonParameters</span></span>
<span data-ttu-id="268f6-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="268f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268f6-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268f6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268f6-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="268f6-121">INPUTS</span></span>

## <span data-ttu-id="268f6-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="268f6-122">OUTPUTS</span></span>

### <span data-ttu-id="268f6-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="268f6-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="268f6-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="268f6-124">NOTES</span></span>

## <span data-ttu-id="268f6-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="268f6-125">RELATED LINKS</span></span>


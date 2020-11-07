---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731675"
---
# <span data-ttu-id="573fd-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="573fd-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="573fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="573fd-102">SYNOPSIS</span></span>
<span data-ttu-id="573fd-103">Создает экземпляр PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="573fd-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="573fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="573fd-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="573fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="573fd-105">DESCRIPTION</span></span>
<span data-ttu-id="573fd-106">Командлет **New-AzApiManagementContext** создает экземпляр класса **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="573fd-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="573fd-107">Контекст используется для всех командлетов службы управления API.</span><span class="sxs-lookup"><span data-stu-id="573fd-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="573fd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="573fd-108">EXAMPLES</span></span>

### <span data-ttu-id="573fd-109">Пример 1: создание экземпляра PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="573fd-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="573fd-110">Эта команда создает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="573fd-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="573fd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="573fd-111">PARAMETERS</span></span>

### <span data-ttu-id="573fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573fd-112">-DefaultProfile</span></span>
<span data-ttu-id="573fd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="573fd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="573fd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573fd-114">-ResourceGroupName</span></span>
<span data-ttu-id="573fd-115">Указывает имя группы ресурсов, в которой развернута служба управления API.</span><span class="sxs-lookup"><span data-stu-id="573fd-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="573fd-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="573fd-116">-ServiceName</span></span>
<span data-ttu-id="573fd-117">Указывает имя развернутой службы управления API.</span><span class="sxs-lookup"><span data-stu-id="573fd-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="573fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573fd-118">CommonParameters</span></span>
<span data-ttu-id="573fd-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="573fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573fd-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573fd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573fd-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="573fd-121">INPUTS</span></span>

### <span data-ttu-id="573fd-122">System. String</span><span class="sxs-lookup"><span data-stu-id="573fd-122">System.String</span></span>

## <span data-ttu-id="573fd-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="573fd-123">OUTPUTS</span></span>

### <span data-ttu-id="573fd-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="573fd-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="573fd-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="573fd-125">NOTES</span></span>

## <span data-ttu-id="573fd-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="573fd-126">RELATED LINKS</span></span>

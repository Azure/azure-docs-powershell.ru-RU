---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393220"
---
# <span data-ttu-id="f2f0e-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="f2f0e-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="f2f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f0e-103">Получает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="f2f0e-103">Gets subscription keys.</span></span>

## <span data-ttu-id="f2f0e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2f0e-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2f0e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="f2f0e-106">Для получения ключей указанной подписки можно получить ключ от **get-AzApiManagementSubscriptionKey.**</span><span class="sxs-lookup"><span data-stu-id="f2f0e-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="f2f0e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2f0e-107">EXAMPLES</span></span>

### <span data-ttu-id="f2f0e-108">Пример 1. Получите ключи подписки с указанным ИД</span><span class="sxs-lookup"><span data-stu-id="f2f0e-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="f2f0e-109">Эта команда получает подписку по ИД.</span><span class="sxs-lookup"><span data-stu-id="f2f0e-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="f2f0e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2f0e-110">PARAMETERS</span></span>

### <span data-ttu-id="f2f0e-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f2f0e-111">-Context</span></span>
<span data-ttu-id="f2f0e-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f2f0e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f2f0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f0e-113">-DefaultProfile</span></span>
<span data-ttu-id="f2f0e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f0e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2f0e-115">-SubscriptionId</span></span>
<span data-ttu-id="f2f0e-116">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f2f0e-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="f2f0e-117">Если он задан, этот cmdlet находит подписку по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="f2f0e-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="f2f0e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f0e-118">CommonParameters</span></span>
<span data-ttu-id="f2f0e-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f0e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f0e-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2f0e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f0e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2f0e-121">INPUTS</span></span>

### <span data-ttu-id="f2f0e-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f2f0e-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f2f0e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f2f0e-123">System.String</span></span>

## <span data-ttu-id="f2f0e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2f0e-124">OUTPUTS</span></span>

### <span data-ttu-id="f2f0e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="f2f0e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="f2f0e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2f0e-126">NOTES</span></span>

## <span data-ttu-id="f2f0e-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2f0e-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2f0e-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f2f0e-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="f2f0e-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f2f0e-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="f2f0e-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f2f0e-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="f2f0e-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f2f0e-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)



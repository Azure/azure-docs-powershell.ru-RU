---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566349"
---
# <span data-ttu-id="a2479-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a2479-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="a2479-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2479-102">SYNOPSIS</span></span>
<span data-ttu-id="a2479-103">Получает сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="a2479-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2479-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2479-104">SYNTAX</span></span>

### <span data-ttu-id="a2479-105">Получение сервера авторизации (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2479-105">Get all authorization server (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2479-106">Получить по идентификатору</span><span class="sxs-lookup"><span data-stu-id="a2479-106">Get by Id</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2479-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2479-107">DESCRIPTION</span></span>
<span data-ttu-id="a2479-108">Командлет **Get-AzureRmApiManagementAuthorizationServer** получает все серверы авторизации управления правами на доступ к управлению API Azure или указанные серверы авторизации.</span><span class="sxs-lookup"><span data-stu-id="a2479-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="a2479-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2479-109">EXAMPLES</span></span>

### <span data-ttu-id="a2479-110">Пример 1: получение всех серверов авторизации</span><span class="sxs-lookup"><span data-stu-id="a2479-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="a2479-111">Эта команда получает все серверы авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="a2479-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="a2479-112">Пример 2: получение указанного сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="a2479-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="a2479-113">Эта команда получает указанный сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="a2479-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="a2479-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2479-114">PARAMETERS</span></span>

### <span data-ttu-id="a2479-115">-Context</span><span class="sxs-lookup"><span data-stu-id="a2479-115">-Context</span></span>
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

### <span data-ttu-id="a2479-116">-ServerId</span><span class="sxs-lookup"><span data-stu-id="a2479-116">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2479-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2479-117">-DefaultProfile</span></span>
<span data-ttu-id="a2479-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2479-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2479-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2479-119">CommonParameters</span></span>
<span data-ttu-id="a2479-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2479-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2479-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2479-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2479-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2479-122">INPUTS</span></span>

## <span data-ttu-id="a2479-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2479-123">OUTPUTS</span></span>

### <span data-ttu-id="a2479-124">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="a2479-124">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>

## <span data-ttu-id="a2479-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2479-125">NOTES</span></span>

## <span data-ttu-id="a2479-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2479-126">RELATED LINKS</span></span>

[<span data-ttu-id="a2479-127">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a2479-127">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="a2479-128">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a2479-128">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="a2479-129">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a2479-129">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)



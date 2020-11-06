---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565975"
---
# <span data-ttu-id="3cd94-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="3cd94-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="3cd94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cd94-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd94-103">Создание URL-адреса SSO для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3cd94-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cd94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cd94-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cd94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cd94-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd94-106">Командлет **Get-AzureRmApiManagementUserSsoUrl** создает для пользователя URL-адрес единого входа.</span><span class="sxs-lookup"><span data-stu-id="3cd94-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="3cd94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cd94-107">EXAMPLES</span></span>

### <span data-ttu-id="3cd94-108">Пример 1: получение URL-адреса пользователя для единого входа</span><span class="sxs-lookup"><span data-stu-id="3cd94-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="3cd94-109">Эта команда получает URL-адрес пользователя SSO.</span><span class="sxs-lookup"><span data-stu-id="3cd94-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="3cd94-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cd94-110">PARAMETERS</span></span>

### <span data-ttu-id="3cd94-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3cd94-111">-Context</span></span>
<span data-ttu-id="3cd94-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3cd94-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="3cd94-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3cd94-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3cd94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd94-114">-DefaultProfile</span></span>
<span data-ttu-id="3cd94-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cd94-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cd94-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="3cd94-116">-UserId</span></span>
<span data-ttu-id="3cd94-117">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="3cd94-117">Specifies a user ID.</span></span>
<span data-ttu-id="3cd94-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3cd94-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3cd94-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd94-119">CommonParameters</span></span>
<span data-ttu-id="3cd94-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cd94-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd94-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd94-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd94-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cd94-122">INPUTS</span></span>

### <span data-ttu-id="3cd94-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3cd94-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3cd94-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3cd94-124">System.String</span></span>

## <span data-ttu-id="3cd94-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cd94-125">OUTPUTS</span></span>

### <span data-ttu-id="3cd94-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3cd94-126">System.String</span></span>

## <span data-ttu-id="3cd94-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cd94-127">NOTES</span></span>

## <span data-ttu-id="3cd94-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cd94-128">RELATED LINKS</span></span>

[<span data-ttu-id="3cd94-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3cd94-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)



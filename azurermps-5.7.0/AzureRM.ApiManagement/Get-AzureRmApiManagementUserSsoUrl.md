---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 5cc7eb81c9ccaf461b1f2ab16e76aa662ea0f57b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563772"
---
# <span data-ttu-id="ce039-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="ce039-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="ce039-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce039-102">SYNOPSIS</span></span>
<span data-ttu-id="ce039-103">Создание URL-адреса SSO для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ce039-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce039-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce039-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce039-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce039-105">DESCRIPTION</span></span>
<span data-ttu-id="ce039-106">Командлет **Get-AzureRmApiManagementUserSsoUrl** создает для пользователя URL-адрес единого входа.</span><span class="sxs-lookup"><span data-stu-id="ce039-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="ce039-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce039-107">EXAMPLES</span></span>

### <span data-ttu-id="ce039-108">Пример 1: получение URL-адреса пользователя для единого входа</span><span class="sxs-lookup"><span data-stu-id="ce039-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ce039-109">Эта команда получает URL-адрес пользователя SSO.</span><span class="sxs-lookup"><span data-stu-id="ce039-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="ce039-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce039-110">PARAMETERS</span></span>

### <span data-ttu-id="ce039-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ce039-111">-Context</span></span>
<span data-ttu-id="ce039-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ce039-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ce039-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ce039-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ce039-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce039-114">-DefaultProfile</span></span>
<span data-ttu-id="ce039-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce039-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce039-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="ce039-116">-UserId</span></span>
<span data-ttu-id="ce039-117">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="ce039-117">Specifies a user ID.</span></span>
<span data-ttu-id="ce039-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ce039-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ce039-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce039-119">CommonParameters</span></span>
<span data-ttu-id="ce039-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce039-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce039-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce039-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce039-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce039-122">INPUTS</span></span>

### <span data-ttu-id="ce039-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="ce039-123">None</span></span>
<span data-ttu-id="ce039-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ce039-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce039-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce039-125">OUTPUTS</span></span>

### <span data-ttu-id="ce039-126">подстрок</span><span class="sxs-lookup"><span data-stu-id="ce039-126">string</span></span>

## <span data-ttu-id="ce039-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce039-127">NOTES</span></span>

## <span data-ttu-id="ce039-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce039-128">RELATED LINKS</span></span>

[<span data-ttu-id="ce039-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ce039-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)



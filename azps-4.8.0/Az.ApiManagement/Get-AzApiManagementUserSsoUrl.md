---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078004"
---
# <span data-ttu-id="f98c1-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="f98c1-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="f98c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f98c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f98c1-103">Создание URL-адреса SSO для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f98c1-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="f98c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f98c1-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f98c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f98c1-105">DESCRIPTION</span></span>
<span data-ttu-id="f98c1-106">Командлет **Get-AzApiManagementUserSsoUrl** создает для пользователя URL-адрес единого входа.</span><span class="sxs-lookup"><span data-stu-id="f98c1-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="f98c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f98c1-107">EXAMPLES</span></span>

### <span data-ttu-id="f98c1-108">Пример 1: получение URL-адреса пользователя для единого входа</span><span class="sxs-lookup"><span data-stu-id="f98c1-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f98c1-109">Эта команда получает URL-адрес пользователя SSO.</span><span class="sxs-lookup"><span data-stu-id="f98c1-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="f98c1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f98c1-110">PARAMETERS</span></span>

### <span data-ttu-id="f98c1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f98c1-111">-Context</span></span>
<span data-ttu-id="f98c1-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f98c1-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f98c1-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f98c1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f98c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98c1-114">-DefaultProfile</span></span>
<span data-ttu-id="f98c1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f98c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f98c1-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="f98c1-116">-UserId</span></span>
<span data-ttu-id="f98c1-117">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="f98c1-117">Specifies a user ID.</span></span>
<span data-ttu-id="f98c1-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f98c1-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f98c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98c1-119">CommonParameters</span></span>
<span data-ttu-id="f98c1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f98c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98c1-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f98c1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98c1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f98c1-122">INPUTS</span></span>

### <span data-ttu-id="f98c1-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f98c1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f98c1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f98c1-124">System.String</span></span>

## <span data-ttu-id="f98c1-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f98c1-125">OUTPUTS</span></span>

### <span data-ttu-id="f98c1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f98c1-126">System.String</span></span>

## <span data-ttu-id="f98c1-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f98c1-127">NOTES</span></span>

## <span data-ttu-id="f98c1-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f98c1-128">RELATED LINKS</span></span>

[<span data-ttu-id="f98c1-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f98c1-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)



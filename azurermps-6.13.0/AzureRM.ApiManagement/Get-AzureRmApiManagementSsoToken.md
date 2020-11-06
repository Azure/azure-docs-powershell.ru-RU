---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: e0bce4f579b2000bc970e35ceb03da03fdffb211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556975"
---
# <span data-ttu-id="30891-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="30891-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="30891-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30891-102">SYNOPSIS</span></span>
<span data-ttu-id="30891-103">Возвращает ссылку с маркером единого входа на развернутый портал управления в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="30891-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30891-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30891-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30891-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30891-105">DESCRIPTION</span></span>
<span data-ttu-id="30891-106">Командлет **Get-AzureRmApiManagementSsoToken** возвращает ссылку (URL-адрес), содержащую маркер единого входа (SSO), на развернутый портал управления для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="30891-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="30891-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30891-107">EXAMPLES</span></span>

### <span data-ttu-id="30891-108">Пример 1: получение маркера единого входа для службы управления API</span><span class="sxs-lookup"><span data-stu-id="30891-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="30891-109">Эта команда получает маркер SSO службы управления API.</span><span class="sxs-lookup"><span data-stu-id="30891-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="30891-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30891-110">PARAMETERS</span></span>

### <span data-ttu-id="30891-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30891-111">-DefaultProfile</span></span>
<span data-ttu-id="30891-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30891-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30891-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30891-113">-Name</span></span>
<span data-ttu-id="30891-114">Указывает имя экземпляра управления API.</span><span class="sxs-lookup"><span data-stu-id="30891-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="30891-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30891-115">-ResourceGroupName</span></span>
<span data-ttu-id="30891-116">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="30891-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="30891-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30891-117">CommonParameters</span></span>
<span data-ttu-id="30891-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30891-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30891-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30891-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30891-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30891-120">INPUTS</span></span>

### <span data-ttu-id="30891-121">System. String</span><span class="sxs-lookup"><span data-stu-id="30891-121">System.String</span></span>

## <span data-ttu-id="30891-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30891-122">OUTPUTS</span></span>

### <span data-ttu-id="30891-123">System. String</span><span class="sxs-lookup"><span data-stu-id="30891-123">System.String</span></span>

## <span data-ttu-id="30891-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="30891-124">NOTES</span></span>

## <span data-ttu-id="30891-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30891-125">RELATED LINKS</span></span>

[<span data-ttu-id="30891-126">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="30891-126">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)



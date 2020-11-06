---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 30243ef1796e621d0898aae38e29ddb1dc7fd20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568362"
---
# <span data-ttu-id="59d03-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="59d03-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="59d03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59d03-102">SYNOPSIS</span></span>
<span data-ttu-id="59d03-103">Получает конфигурацию доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="59d03-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59d03-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59d03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d03-105">DESCRIPTION</span></span>
<span data-ttu-id="59d03-106">Командлет **Get-AzureRmApiManagementTenantAccess** получает конфигурацию доступа клиента для клиента.</span><span class="sxs-lookup"><span data-stu-id="59d03-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="59d03-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59d03-107">EXAMPLES</span></span>

### <span data-ttu-id="59d03-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="59d03-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $ApimContext
```

<span data-ttu-id="59d03-109">Эта команда получает конфигурацию доступа клиента для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="59d03-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="59d03-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59d03-110">PARAMETERS</span></span>

### <span data-ttu-id="59d03-111">-Context</span><span class="sxs-lookup"><span data-stu-id="59d03-111">-Context</span></span>
<span data-ttu-id="59d03-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="59d03-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="59d03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d03-113">-DefaultProfile</span></span>
<span data-ttu-id="59d03-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59d03-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59d03-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d03-115">CommonParameters</span></span>
<span data-ttu-id="59d03-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59d03-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d03-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d03-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d03-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59d03-118">INPUTS</span></span>

## <span data-ttu-id="59d03-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d03-119">OUTPUTS</span></span>

### <span data-ttu-id="59d03-120">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="59d03-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="59d03-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="59d03-121">NOTES</span></span>

## <span data-ttu-id="59d03-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59d03-122">RELATED LINKS</span></span>

[<span data-ttu-id="59d03-123">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="59d03-123">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)



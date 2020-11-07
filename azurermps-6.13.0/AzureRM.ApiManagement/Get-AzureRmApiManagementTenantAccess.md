---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 010e52d7c2d05977c8125d5d78d69ef8ac7f75fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731996"
---
# <span data-ttu-id="b13f5-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b13f5-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="b13f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b13f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b13f5-103">Получает конфигурацию доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="b13f5-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b13f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b13f5-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b13f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b13f5-105">DESCRIPTION</span></span>
<span data-ttu-id="b13f5-106">Командлет **Get-AzureRmApiManagementTenantAccess** получает конфигурацию доступа клиента для клиента.</span><span class="sxs-lookup"><span data-stu-id="b13f5-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="b13f5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b13f5-107">EXAMPLES</span></span>

### <span data-ttu-id="b13f5-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="b13f5-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="b13f5-109">Эта команда получает конфигурацию доступа клиента для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="b13f5-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="b13f5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b13f5-110">PARAMETERS</span></span>

### <span data-ttu-id="b13f5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b13f5-111">-Context</span></span>
<span data-ttu-id="b13f5-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b13f5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b13f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13f5-113">-DefaultProfile</span></span>
<span data-ttu-id="b13f5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b13f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b13f5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13f5-115">CommonParameters</span></span>
<span data-ttu-id="b13f5-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b13f5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13f5-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13f5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13f5-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b13f5-118">INPUTS</span></span>

### <span data-ttu-id="b13f5-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b13f5-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b13f5-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b13f5-120">OUTPUTS</span></span>

### <span data-ttu-id="b13f5-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b13f5-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b13f5-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="b13f5-122">NOTES</span></span>

## <span data-ttu-id="b13f5-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b13f5-123">RELATED LINKS</span></span>

[<span data-ttu-id="b13f5-124">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b13f5-124">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)



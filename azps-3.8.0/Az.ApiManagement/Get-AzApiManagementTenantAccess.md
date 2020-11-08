---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 3c4151cbc6b170f8b34e70126f37e4478933744d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065402"
---
# <span data-ttu-id="3c7ad-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="3c7ad-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="3c7ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7ad-103">Получает конфигурацию доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="3c7ad-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="3c7ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c7ad-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c7ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7ad-105">DESCRIPTION</span></span>
<span data-ttu-id="3c7ad-106">Командлет **Get-AzApiManagementTenantAccess** получает конфигурацию доступа клиента для клиента.</span><span class="sxs-lookup"><span data-stu-id="3c7ad-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="3c7ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c7ad-107">EXAMPLES</span></span>

### <span data-ttu-id="3c7ad-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="3c7ad-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="3c7ad-109">Эта команда получает конфигурацию доступа клиента для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="3c7ad-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="3c7ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c7ad-110">PARAMETERS</span></span>

### <span data-ttu-id="3c7ad-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3c7ad-111">-Context</span></span>
<span data-ttu-id="3c7ad-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3c7ad-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3c7ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7ad-113">-DefaultProfile</span></span>
<span data-ttu-id="3c7ad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7ad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7ad-115">CommonParameters</span></span>
<span data-ttu-id="3c7ad-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c7ad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7ad-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c7ad-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7ad-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c7ad-118">INPUTS</span></span>

### <span data-ttu-id="3c7ad-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3c7ad-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3c7ad-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7ad-120">OUTPUTS</span></span>

### <span data-ttu-id="3c7ad-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3c7ad-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3c7ad-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c7ad-122">NOTES</span></span>

## <span data-ttu-id="3c7ad-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c7ad-123">RELATED LINKS</span></span>

[<span data-ttu-id="3c7ad-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="3c7ad-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)



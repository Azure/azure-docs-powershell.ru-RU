---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316793"
---
# <span data-ttu-id="2990b-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2990b-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="2990b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2990b-102">SYNOPSIS</span></span>
<span data-ttu-id="2990b-103">Получает конфигурацию доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="2990b-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="2990b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2990b-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2990b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2990b-105">DESCRIPTION</span></span>
<span data-ttu-id="2990b-106">Командлет **Get-AzApiManagementTenantAccess** получает конфигурацию доступа клиента для клиента.</span><span class="sxs-lookup"><span data-stu-id="2990b-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="2990b-107">Ключи не будут включены в данные результата.</span><span class="sxs-lookup"><span data-stu-id="2990b-107">Keys will not be included into result details.</span></span> <span data-ttu-id="2990b-108">Чтобы получить секрет клиента, используйте **Get-AzApiManagementTenantAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="2990b-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="2990b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2990b-109">EXAMPLES</span></span>

### <span data-ttu-id="2990b-110">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="2990b-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="2990b-111">Эта команда получает конфигурацию доступа клиента для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="2990b-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="2990b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2990b-112">PARAMETERS</span></span>

### <span data-ttu-id="2990b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2990b-113">-Context</span></span>
<span data-ttu-id="2990b-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2990b-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2990b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2990b-115">-DefaultProfile</span></span>
<span data-ttu-id="2990b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2990b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2990b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2990b-117">CommonParameters</span></span>
<span data-ttu-id="2990b-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2990b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2990b-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2990b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2990b-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2990b-120">INPUTS</span></span>

### <span data-ttu-id="2990b-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2990b-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="2990b-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2990b-122">OUTPUTS</span></span>

### <span data-ttu-id="2990b-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="2990b-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="2990b-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="2990b-124">NOTES</span></span>

## <span data-ttu-id="2990b-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2990b-125">RELATED LINKS</span></span>

[<span data-ttu-id="2990b-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2990b-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 8c01d617f214df5e505e060d1f0cf1665a9f12bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728087"
---
# <span data-ttu-id="ef3fd-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="ef3fd-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="ef3fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3fd-103">Получает конфигурацию доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="ef3fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef3fd-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef3fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="ef3fd-106">Командлет **Get-AzApiManagementTenantAccess** получает конфигурацию доступа клиента для клиента.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="ef3fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef3fd-107">EXAMPLES</span></span>

### <span data-ttu-id="ef3fd-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="ef3fd-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="ef3fd-109">Эта команда получает конфигурацию доступа клиента для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="ef3fd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef3fd-110">PARAMETERS</span></span>

### <span data-ttu-id="ef3fd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ef3fd-111">-Context</span></span>
<span data-ttu-id="ef3fd-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ef3fd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ef3fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3fd-113">-DefaultProfile</span></span>
<span data-ttu-id="ef3fd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef3fd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3fd-115">CommonParameters</span></span>
<span data-ttu-id="ef3fd-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3fd-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef3fd-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3fd-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef3fd-118">INPUTS</span></span>

### <span data-ttu-id="ef3fd-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ef3fd-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="ef3fd-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef3fd-120">OUTPUTS</span></span>

### <span data-ttu-id="ef3fd-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="ef3fd-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="ef3fd-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef3fd-122">NOTES</span></span>

## <span data-ttu-id="ef3fd-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef3fd-123">RELATED LINKS</span></span>

[<span data-ttu-id="ef3fd-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="ef3fd-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)



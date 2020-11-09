---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248262"
---
# <span data-ttu-id="681d4-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="681d4-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="681d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="681d4-102">SYNOPSIS</span></span>
<span data-ttu-id="681d4-103">Получает ключи конфигурации доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="681d4-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="681d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="681d4-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="681d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="681d4-105">DESCRIPTION</span></span>
<span data-ttu-id="681d4-106">Получает ключи конфигурации доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="681d4-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="681d4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="681d4-107">EXAMPLES</span></span>

### <span data-ttu-id="681d4-108">Пример 1: получение ключей конфигурации для доступа к клиенту</span><span class="sxs-lookup"><span data-stu-id="681d4-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="681d4-109">Эта команда получает ключи конфигурации для доступа клиента к заданному контексту.</span><span class="sxs-lookup"><span data-stu-id="681d4-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="681d4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="681d4-110">PARAMETERS</span></span>

### <span data-ttu-id="681d4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="681d4-111">-Context</span></span>
<span data-ttu-id="681d4-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="681d4-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="681d4-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="681d4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="681d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681d4-114">-DefaultProfile</span></span>
<span data-ttu-id="681d4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="681d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="681d4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681d4-116">CommonParameters</span></span>
<span data-ttu-id="681d4-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="681d4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681d4-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="681d4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681d4-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="681d4-119">INPUTS</span></span>

### <span data-ttu-id="681d4-120">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="681d4-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="681d4-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="681d4-121">OUTPUTS</span></span>

### <span data-ttu-id="681d4-122">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="681d4-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="681d4-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="681d4-123">NOTES</span></span>

## <span data-ttu-id="681d4-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="681d4-124">RELATED LINKS</span></span>
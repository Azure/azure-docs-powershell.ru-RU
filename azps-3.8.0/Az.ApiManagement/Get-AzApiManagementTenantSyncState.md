---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072853"
---
# <span data-ttu-id="cef91-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="cef91-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="cef91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cef91-102">SYNOPSIS</span></span>
<span data-ttu-id="cef91-103">Возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="cef91-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="cef91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cef91-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cef91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef91-105">DESCRIPTION</span></span>
<span data-ttu-id="cef91-106">Командлет **Get-AzApiManagementTenantSyncState** возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="cef91-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="cef91-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cef91-107">EXAMPLES</span></span>

### <span data-ttu-id="cef91-108">Пример 1: получение состояния последней синхронизации</span><span class="sxs-lookup"><span data-stu-id="cef91-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="cef91-109">Эта команда возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="cef91-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="cef91-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cef91-110">PARAMETERS</span></span>

### <span data-ttu-id="cef91-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cef91-111">-Context</span></span>
<span data-ttu-id="cef91-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cef91-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cef91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef91-113">-DefaultProfile</span></span>
<span data-ttu-id="cef91-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cef91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cef91-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef91-115">CommonParameters</span></span>
<span data-ttu-id="cef91-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cef91-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef91-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cef91-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef91-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cef91-118">INPUTS</span></span>

### <span data-ttu-id="cef91-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cef91-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="cef91-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef91-120">OUTPUTS</span></span>

### <span data-ttu-id="cef91-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="cef91-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="cef91-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="cef91-122">NOTES</span></span>

## <span data-ttu-id="cef91-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef91-123">RELATED LINKS</span></span>

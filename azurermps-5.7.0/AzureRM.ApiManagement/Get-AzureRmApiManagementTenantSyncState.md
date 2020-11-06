---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: 64e1d8ad070d4ce1c2f8129a73efd8730f26d1a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563780"
---
# <span data-ttu-id="a9d23-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="a9d23-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="a9d23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9d23-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d23-103">Возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="a9d23-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9d23-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9d23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9d23-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d23-106">Командлет **Get-AzureRmApiManagementTenantSyncState** возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="a9d23-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="a9d23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9d23-107">EXAMPLES</span></span>

### <span data-ttu-id="a9d23-108">Пример 1: получение состояния последней синхронизации</span><span class="sxs-lookup"><span data-stu-id="a9d23-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext 
```

<span data-ttu-id="a9d23-109">Эта команда возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="a9d23-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="a9d23-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9d23-110">PARAMETERS</span></span>

### <span data-ttu-id="a9d23-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a9d23-111">-Context</span></span>
<span data-ttu-id="a9d23-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a9d23-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a9d23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d23-113">-DefaultProfile</span></span>
<span data-ttu-id="a9d23-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a9d23-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d23-115">CommonParameters</span></span>
<span data-ttu-id="a9d23-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9d23-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d23-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d23-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d23-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9d23-118">INPUTS</span></span>

### <span data-ttu-id="a9d23-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="a9d23-119">None</span></span>
<span data-ttu-id="a9d23-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a9d23-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9d23-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9d23-121">OUTPUTS</span></span>

### <span data-ttu-id="a9d23-122">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="a9d23-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="a9d23-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9d23-123">NOTES</span></span>

## <span data-ttu-id="a9d23-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9d23-124">RELATED LINKS</span></span>


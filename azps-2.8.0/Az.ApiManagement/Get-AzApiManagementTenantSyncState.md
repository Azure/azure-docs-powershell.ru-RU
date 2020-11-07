---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: c8d3ff0d268c4a84269585af7e769b46af663f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728085"
---
# <span data-ttu-id="0660e-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="0660e-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="0660e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0660e-102">SYNOPSIS</span></span>
<span data-ttu-id="0660e-103">Возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="0660e-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="0660e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0660e-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0660e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0660e-105">DESCRIPTION</span></span>
<span data-ttu-id="0660e-106">Командлет **Get-AzApiManagementTenantSyncState** возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="0660e-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="0660e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0660e-107">EXAMPLES</span></span>

### <span data-ttu-id="0660e-108">Пример 1: получение состояния последней синхронизации</span><span class="sxs-lookup"><span data-stu-id="0660e-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="0660e-109">Эта команда возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="0660e-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="0660e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0660e-110">PARAMETERS</span></span>

### <span data-ttu-id="0660e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0660e-111">-Context</span></span>
<span data-ttu-id="0660e-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0660e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0660e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0660e-113">-DefaultProfile</span></span>
<span data-ttu-id="0660e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0660e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0660e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0660e-115">CommonParameters</span></span>
<span data-ttu-id="0660e-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0660e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0660e-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0660e-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0660e-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0660e-118">INPUTS</span></span>

### <span data-ttu-id="0660e-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0660e-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="0660e-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0660e-120">OUTPUTS</span></span>

### <span data-ttu-id="0660e-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="0660e-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="0660e-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="0660e-122">NOTES</span></span>

## <span data-ttu-id="0660e-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0660e-123">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074224"
---
# <span data-ttu-id="cb5bb-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb5bb-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="cb5bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5bb-103">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="cb5bb-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="cb5bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb5bb-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb5bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb5bb-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5bb-106">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="cb5bb-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="cb5bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb5bb-107">EXAMPLES</span></span>

### <span data-ttu-id="cb5bb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb5bb-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="cb5bb-109">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="cb5bb-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="cb5bb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb5bb-110">PARAMETERS</span></span>

### <span data-ttu-id="cb5bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5bb-111">-DefaultProfile</span></span>
<span data-ttu-id="cb5bb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb5bb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb5bb-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb5bb-113">-Name</span></span>
<span data-ttu-id="cb5bb-114">Имя конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cb5bb-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb5bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb5bb-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb5bb-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb5bb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5bb-117">CommonParameters</span></span>
<span data-ttu-id="cb5bb-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb5bb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5bb-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb5bb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5bb-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb5bb-120">INPUTS</span></span>

### <span data-ttu-id="cb5bb-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cb5bb-121">System.String</span></span>

## <span data-ttu-id="cb5bb-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb5bb-122">OUTPUTS</span></span>

### <span data-ttu-id="cb5bb-123">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb5bb-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="cb5bb-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb5bb-124">NOTES</span></span>

## <span data-ttu-id="cb5bb-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb5bb-125">RELATED LINKS</span></span>

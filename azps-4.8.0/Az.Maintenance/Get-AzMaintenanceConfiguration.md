---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236121"
---
# <span data-ttu-id="ef9c5-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef9c5-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="ef9c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9c5-103">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="ef9c5-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="ef9c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef9c5-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef9c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef9c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ef9c5-106">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="ef9c5-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="ef9c5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef9c5-107">EXAMPLES</span></span>

### <span data-ttu-id="ef9c5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef9c5-108">Example 1</span></span>
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

<span data-ttu-id="ef9c5-109">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="ef9c5-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="ef9c5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef9c5-110">PARAMETERS</span></span>

### <span data-ttu-id="ef9c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef9c5-111">-DefaultProfile</span></span>
<span data-ttu-id="ef9c5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef9c5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef9c5-113">-Name</span></span>
<span data-ttu-id="ef9c5-114">Имя конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="ef9c5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef9c5-115">-ResourceGroupName</span></span>
<span data-ttu-id="ef9c5-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="ef9c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9c5-117">CommonParameters</span></span>
<span data-ttu-id="ef9c5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9c5-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef9c5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9c5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef9c5-120">INPUTS</span></span>

### <span data-ttu-id="ef9c5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ef9c5-121">System.String</span></span>

## <span data-ttu-id="ef9c5-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef9c5-122">OUTPUTS</span></span>

### <span data-ttu-id="ef9c5-123">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef9c5-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="ef9c5-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef9c5-124">NOTES</span></span>

## <span data-ttu-id="ef9c5-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef9c5-125">RELATED LINKS</span></span>

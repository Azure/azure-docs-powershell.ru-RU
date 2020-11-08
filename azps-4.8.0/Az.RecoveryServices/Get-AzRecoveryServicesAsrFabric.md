---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244021"
---
# <span data-ttu-id="ae3d7-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ae3d7-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="ae3d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3d7-103">Получение сведений о структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="ae3d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae3d7-104">SYNTAX</span></span>

### <span data-ttu-id="ae3d7-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae3d7-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae3d7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ae3d7-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae3d7-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ae3d7-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae3d7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae3d7-108">DESCRIPTION</span></span>
<span data-ttu-id="ae3d7-109">Командлет **Get-AzRecoveryServicesAsrFabric** получает свойства указанной структуры восстановления сайта Azure или всех структур восстановления сайта Azure в хранилище службы восстановления.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="ae3d7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae3d7-110">EXAMPLES</span></span>

### <span data-ttu-id="ae3d7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae3d7-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="ae3d7-112">Возвращает все структуры восстановления сайта Azure в хранилище.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="ae3d7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ae3d7-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="ae3d7-114">Возвращают структуру восстановления сайта Azure с именем XXXX.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="ae3d7-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ae3d7-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="ae3d7-116">Возвращают структуру восстановления сайта Azure с понятным именем XXXX.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="ae3d7-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae3d7-117">PARAMETERS</span></span>

### <span data-ttu-id="ae3d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3d7-118">-DefaultProfile</span></span>
<span data-ttu-id="ae3d7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae3d7-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ae3d7-120">-FriendlyName</span></span>
<span data-ttu-id="ae3d7-121">Найдите структуру ASR с помощью понятного имени структуры.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3d7-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae3d7-122">-Name</span></span>
<span data-ttu-id="ae3d7-123">Найдите структуру ASR с помощью имени структуры.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3d7-124">CommonParameters</span></span>
<span data-ttu-id="ae3d7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae3d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3d7-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae3d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3d7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae3d7-127">INPUTS</span></span>

### <span data-ttu-id="ae3d7-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="ae3d7-128">None</span></span>

## <span data-ttu-id="ae3d7-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae3d7-129">OUTPUTS</span></span>

### <span data-ttu-id="ae3d7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ae3d7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ae3d7-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae3d7-131">NOTES</span></span>

## <span data-ttu-id="ae3d7-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae3d7-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae3d7-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ae3d7-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="ae3d7-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ae3d7-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)

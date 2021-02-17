---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236145"
---
# <span data-ttu-id="bacf5-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bacf5-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="bacf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bacf5-102">SYNOPSIS</span></span>
<span data-ttu-id="bacf5-103">Получите сведения о структуре для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="bacf5-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="bacf5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bacf5-104">SYNTAX</span></span>

### <span data-ttu-id="bacf5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bacf5-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bacf5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bacf5-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bacf5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="bacf5-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bacf5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bacf5-108">DESCRIPTION</span></span>
<span data-ttu-id="bacf5-109">Для получения свойств указанной тканью для восстановления сайта Azure или всеми тканью для восстановления сайтов Azure в хранилище службы восстановления может быть задана **cmdlet Get-AzRecoveryServicesAsrFabric.**</span><span class="sxs-lookup"><span data-stu-id="bacf5-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="bacf5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bacf5-110">EXAMPLES</span></span>

### <span data-ttu-id="bacf5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bacf5-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="bacf5-112">Возвращает все ткань для восстановления сайта Azure в сейфе.</span><span class="sxs-lookup"><span data-stu-id="bacf5-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="bacf5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bacf5-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="bacf5-114">Возврат материала восстановления сайта Azure с именем xxxx.</span><span class="sxs-lookup"><span data-stu-id="bacf5-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="bacf5-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bacf5-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="bacf5-116">Возврат материала восстановления сайта Azure с удобным именем xxxx.</span><span class="sxs-lookup"><span data-stu-id="bacf5-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="bacf5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bacf5-117">PARAMETERS</span></span>

### <span data-ttu-id="bacf5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bacf5-118">-DefaultProfile</span></span>
<span data-ttu-id="bacf5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bacf5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bacf5-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bacf5-120">-FriendlyName</span></span>
<span data-ttu-id="bacf5-121">Найщите материал ASR по удобному имени.</span><span class="sxs-lookup"><span data-stu-id="bacf5-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="bacf5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bacf5-122">-Name</span></span>
<span data-ttu-id="bacf5-123">Поищите материал ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="bacf5-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="bacf5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bacf5-124">CommonParameters</span></span>
<span data-ttu-id="bacf5-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bacf5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bacf5-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bacf5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bacf5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bacf5-127">INPUTS</span></span>

### <span data-ttu-id="bacf5-128">Нет</span><span class="sxs-lookup"><span data-stu-id="bacf5-128">None</span></span>

## <span data-ttu-id="bacf5-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bacf5-129">OUTPUTS</span></span>

### <span data-ttu-id="bacf5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bacf5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bacf5-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bacf5-131">NOTES</span></span>

## <span data-ttu-id="bacf5-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bacf5-132">RELATED LINKS</span></span>

[<span data-ttu-id="bacf5-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bacf5-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="bacf5-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="bacf5-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)

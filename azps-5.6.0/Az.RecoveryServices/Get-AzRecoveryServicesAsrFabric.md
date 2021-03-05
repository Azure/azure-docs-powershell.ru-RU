---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1aeaba2f4f25abd49f12d087b7390f5e92f19c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016152"
---
# <span data-ttu-id="50a58-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="50a58-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="50a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50a58-102">SYNOPSIS</span></span>
<span data-ttu-id="50a58-103">Получите подробные сведения о структуре для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="50a58-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="50a58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50a58-104">SYNTAX</span></span>

### <span data-ttu-id="50a58-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50a58-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50a58-106">ByName</span><span class="sxs-lookup"><span data-stu-id="50a58-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50a58-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="50a58-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50a58-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50a58-108">DESCRIPTION</span></span>
<span data-ttu-id="50a58-109">Для получения свойств указанной тканью для восстановления сайта Azure или всеми тканью для восстановления сайтов Azure в хранилище службы восстановления может быть задана cmdlet **Get-AzRecoveryServicesAsrFabric.**</span><span class="sxs-lookup"><span data-stu-id="50a58-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="50a58-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50a58-110">EXAMPLES</span></span>

### <span data-ttu-id="50a58-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50a58-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="50a58-112">Возвращает все ткань для восстановления сайта Azure в сейфе.</span><span class="sxs-lookup"><span data-stu-id="50a58-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="50a58-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="50a58-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="50a58-114">Возврат материала восстановления сайта Azure с именем xxxx.</span><span class="sxs-lookup"><span data-stu-id="50a58-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="50a58-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="50a58-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="50a58-116">Возврат материала восстановления сайта Azure с удобным именем xxxx.</span><span class="sxs-lookup"><span data-stu-id="50a58-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="50a58-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50a58-117">PARAMETERS</span></span>

### <span data-ttu-id="50a58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a58-118">-DefaultProfile</span></span>
<span data-ttu-id="50a58-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50a58-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50a58-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="50a58-120">-FriendlyName</span></span>
<span data-ttu-id="50a58-121">Найщите материал ASR по удобному имени.</span><span class="sxs-lookup"><span data-stu-id="50a58-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="50a58-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50a58-122">-Name</span></span>
<span data-ttu-id="50a58-123">Поищите материал ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="50a58-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="50a58-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a58-124">CommonParameters</span></span>
<span data-ttu-id="50a58-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50a58-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a58-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50a58-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a58-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50a58-127">INPUTS</span></span>

### <span data-ttu-id="50a58-128">Нет</span><span class="sxs-lookup"><span data-stu-id="50a58-128">None</span></span>

## <span data-ttu-id="50a58-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50a58-129">OUTPUTS</span></span>

### <span data-ttu-id="50a58-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="50a58-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="50a58-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50a58-131">NOTES</span></span>

## <span data-ttu-id="50a58-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50a58-132">RELATED LINKS</span></span>

[<span data-ttu-id="50a58-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="50a58-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="50a58-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="50a58-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)

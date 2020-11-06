---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 92631a1a6c5d27953777efe2b6ea158f59da8fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558891"
---
# <span data-ttu-id="043ce-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="043ce-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="043ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="043ce-102">SYNOPSIS</span></span>
<span data-ttu-id="043ce-103">Получение сведений о структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="043ce-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="043ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="043ce-104">SYNTAX</span></span>

### <span data-ttu-id="043ce-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="043ce-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="043ce-106">ByName</span><span class="sxs-lookup"><span data-stu-id="043ce-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="043ce-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="043ce-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="043ce-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="043ce-108">DESCRIPTION</span></span>
<span data-ttu-id="043ce-109">Командлет **Get-AzureRmRecoveryServicesAsrFabric** получает свойства указанной структуры восстановления сайта Azure или всех структур восстановления сайта Azure в хранилище службы восстановления.</span><span class="sxs-lookup"><span data-stu-id="043ce-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="043ce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="043ce-110">EXAMPLES</span></span>

### <span data-ttu-id="043ce-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="043ce-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="043ce-112">Возвращает все структуры восстановления сайта Azure в хранилище.</span><span class="sxs-lookup"><span data-stu-id="043ce-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="043ce-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="043ce-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="043ce-114">Возвращают структуру восстановления сайта Azure с именем XXXX.</span><span class="sxs-lookup"><span data-stu-id="043ce-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="043ce-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="043ce-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="043ce-116">Возвращают структуру восстановления сайта Azure с понятным именем XXXX.</span><span class="sxs-lookup"><span data-stu-id="043ce-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="043ce-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="043ce-117">PARAMETERS</span></span>

### <span data-ttu-id="043ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043ce-118">-DefaultProfile</span></span>
<span data-ttu-id="043ce-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="043ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="043ce-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="043ce-120">-FriendlyName</span></span>
<span data-ttu-id="043ce-121">Найдите структуру ASR с помощью понятного имени структуры.</span><span class="sxs-lookup"><span data-stu-id="043ce-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ce-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="043ce-122">-Name</span></span>
<span data-ttu-id="043ce-123">Найдите структуру ASR с помощью имени структуры.</span><span class="sxs-lookup"><span data-stu-id="043ce-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043ce-124">CommonParameters</span></span>
<span data-ttu-id="043ce-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="043ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043ce-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="043ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043ce-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="043ce-127">INPUTS</span></span>

### <span data-ttu-id="043ce-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="043ce-128">None</span></span>

## <span data-ttu-id="043ce-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="043ce-129">OUTPUTS</span></span>

### <span data-ttu-id="043ce-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="043ce-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="043ce-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="043ce-131">NOTES</span></span>

## <span data-ttu-id="043ce-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="043ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="043ce-133">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="043ce-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="043ce-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="043ce-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)

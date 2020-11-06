---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b95c3ab14d50558ef184beabcd461a59bb1a05ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561611"
---
# <span data-ttu-id="21005-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21005-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="21005-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21005-102">SYNOPSIS</span></span>
<span data-ttu-id="21005-103">Возвращает план восстановления или все планы восстановления в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="21005-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21005-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21005-104">SYNTAX</span></span>

### <span data-ttu-id="21005-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21005-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21005-106">ByName</span><span class="sxs-lookup"><span data-stu-id="21005-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21005-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="21005-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21005-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21005-108">DESCRIPTION</span></span>
<span data-ttu-id="21005-109">Командлет **Get-AzureRmRecoveryServicesAsrRecoveryPlan** получает сведения о указанном плане восстановления или всех планах восстановления в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="21005-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="21005-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21005-110">EXAMPLES</span></span>

### <span data-ttu-id="21005-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21005-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="21005-112">Получает план восстановления с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="21005-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="21005-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21005-113">PARAMETERS</span></span>

### <span data-ttu-id="21005-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21005-114">-DefaultProfile</span></span>
<span data-ttu-id="21005-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21005-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="21005-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="21005-116">-FriendlyName</span></span>
<span data-ttu-id="21005-117">Указывает понятное имя плана восстановления, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="21005-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="21005-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21005-118">-Name</span></span>
<span data-ttu-id="21005-119">Указывает имя плана восстановления, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="21005-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="21005-120">-Path</span><span class="sxs-lookup"><span data-stu-id="21005-120">-Path</span></span>
<span data-ttu-id="21005-121">Указывает путь к файлу, по которому этот командлет сохраняет определение JSON плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="21005-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="21005-122">Определение JSON можно редактировать, чтобы изменить план восстановления и использовать его для обновления плана восстановления с помощью командлета Update-AzureRmRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21005-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21005-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21005-123">CommonParameters</span></span>
<span data-ttu-id="21005-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21005-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21005-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21005-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21005-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21005-126">INPUTS</span></span>

### <span data-ttu-id="21005-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="21005-127">None</span></span>

## <span data-ttu-id="21005-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21005-128">OUTPUTS</span></span>

### <span data-ttu-id="21005-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="21005-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="21005-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="21005-130">NOTES</span></span>

## <span data-ttu-id="21005-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21005-131">RELATED LINKS</span></span>

[<span data-ttu-id="21005-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21005-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="21005-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21005-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="21005-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21005-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)

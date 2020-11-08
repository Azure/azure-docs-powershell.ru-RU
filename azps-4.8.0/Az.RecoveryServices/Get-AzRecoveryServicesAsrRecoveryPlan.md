---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079379"
---
# <span data-ttu-id="38522-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="38522-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="38522-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38522-102">SYNOPSIS</span></span>
<span data-ttu-id="38522-103">Возвращает план восстановления или все планы восстановления в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="38522-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="38522-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38522-104">SYNTAX</span></span>

### <span data-ttu-id="38522-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38522-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38522-106">ByName</span><span class="sxs-lookup"><span data-stu-id="38522-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38522-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="38522-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38522-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38522-108">DESCRIPTION</span></span>
<span data-ttu-id="38522-109">Командлет **Get-AzRecoveryServicesAsrRecoveryPlan** получает сведения о указанном плане восстановления или всех планах восстановления в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="38522-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="38522-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38522-110">EXAMPLES</span></span>

### <span data-ttu-id="38522-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38522-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="38522-112">Получает план восстановления с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="38522-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="38522-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38522-113">PARAMETERS</span></span>

### <span data-ttu-id="38522-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38522-114">-DefaultProfile</span></span>
<span data-ttu-id="38522-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38522-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="38522-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="38522-116">-FriendlyName</span></span>
<span data-ttu-id="38522-117">Указывает понятное имя плана восстановления, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="38522-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="38522-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38522-118">-Name</span></span>
<span data-ttu-id="38522-119">Указывает имя плана восстановления, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="38522-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="38522-120">-Path</span><span class="sxs-lookup"><span data-stu-id="38522-120">-Path</span></span>
<span data-ttu-id="38522-121">Указывает путь к файлу, по которому этот командлет сохраняет определение JSON плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="38522-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="38522-122">Определение JSON можно редактировать, чтобы изменить план восстановления и использовать его для обновления плана восстановления с помощью командлета Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="38522-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38522-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38522-123">CommonParameters</span></span>
<span data-ttu-id="38522-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38522-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38522-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38522-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38522-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38522-126">INPUTS</span></span>

### <span data-ttu-id="38522-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="38522-127">None</span></span>

## <span data-ttu-id="38522-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38522-128">OUTPUTS</span></span>

### <span data-ttu-id="38522-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="38522-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="38522-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="38522-130">NOTES</span></span>

## <span data-ttu-id="38522-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38522-131">RELATED LINKS</span></span>

[<span data-ttu-id="38522-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="38522-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="38522-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="38522-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="38522-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="38522-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: d3470c3984026232fc90d336e22668868311aa9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963816"
---
# <span data-ttu-id="d092c-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d092c-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d092c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d092c-102">SYNOPSIS</span></span>
<span data-ttu-id="d092c-103">Получает план восстановления или все планы восстановления в хранилище служб восстановления</span><span class="sxs-lookup"><span data-stu-id="d092c-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="d092c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d092c-104">SYNTAX</span></span>

### <span data-ttu-id="d092c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d092c-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d092c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d092c-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d092c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d092c-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d092c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d092c-108">DESCRIPTION</span></span>
<span data-ttu-id="d092c-109">Для получения подробных сведений о указанном плане восстановления или всех планах восстановления в хранилище служб восстановления возвращается cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan.**</span><span class="sxs-lookup"><span data-stu-id="d092c-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="d092c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d092c-110">EXAMPLES</span></span>

### <span data-ttu-id="d092c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d092c-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="d092c-112">Возвращает план восстановления с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d092c-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="d092c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d092c-113">PARAMETERS</span></span>

### <span data-ttu-id="d092c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d092c-114">-DefaultProfile</span></span>
<span data-ttu-id="d092c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d092c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d092c-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d092c-116">-FriendlyName</span></span>
<span data-ttu-id="d092c-117">Указывает удобное имя плана восстановления, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="d092c-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="d092c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d092c-118">-Name</span></span>
<span data-ttu-id="d092c-119">Имя плана восстановления, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="d092c-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="d092c-120">-Path</span><span class="sxs-lookup"><span data-stu-id="d092c-120">-Path</span></span>
<span data-ttu-id="d092c-121">Определяет путь к файлу, на который этот cmdlet сохраняет определение json плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="d092c-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="d092c-122">Определение json можно изменить, чтобы изменить его и использовать для обновления плана восстановления с Update-AzRecoveryServicesASRRecoveryPlan-Update-AzRecoveryServicesASRRecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="d092c-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="d092c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d092c-123">CommonParameters</span></span>
<span data-ttu-id="d092c-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d092c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d092c-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d092c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d092c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d092c-126">INPUTS</span></span>

### <span data-ttu-id="d092c-127">Нет</span><span class="sxs-lookup"><span data-stu-id="d092c-127">None</span></span>

## <span data-ttu-id="d092c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d092c-128">OUTPUTS</span></span>

### <span data-ttu-id="d092c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d092c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="d092c-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d092c-130">NOTES</span></span>

## <span data-ttu-id="d092c-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d092c-131">RELATED LINKS</span></span>

[<span data-ttu-id="d092c-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d092c-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d092c-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d092c-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d092c-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d092c-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)

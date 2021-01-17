---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406212"
---
# <span data-ttu-id="2fb05-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2fb05-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2fb05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fb05-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb05-103">Получает план восстановления или все планы восстановления в хранилище служб восстановления</span><span class="sxs-lookup"><span data-stu-id="2fb05-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="2fb05-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2fb05-104">SYNTAX</span></span>

### <span data-ttu-id="2fb05-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fb05-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fb05-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2fb05-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fb05-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2fb05-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fb05-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fb05-108">DESCRIPTION</span></span>
<span data-ttu-id="2fb05-109">Для получения сведений о указанном плане восстановления или всех планах восстановления в хранилище служб восстановления возвращается cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan.**</span><span class="sxs-lookup"><span data-stu-id="2fb05-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="2fb05-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2fb05-110">EXAMPLES</span></span>

### <span data-ttu-id="2fb05-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2fb05-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="2fb05-112">Возвращает план восстановления с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="2fb05-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="2fb05-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fb05-113">PARAMETERS</span></span>

### <span data-ttu-id="2fb05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb05-114">-DefaultProfile</span></span>
<span data-ttu-id="2fb05-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb05-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2fb05-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2fb05-116">-FriendlyName</span></span>
<span data-ttu-id="2fb05-117">Указывает удобное имя плана восстановления, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2fb05-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="2fb05-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2fb05-118">-Name</span></span>
<span data-ttu-id="2fb05-119">Имя плана восстановления, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2fb05-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="2fb05-120">-Path</span><span class="sxs-lookup"><span data-stu-id="2fb05-120">-Path</span></span>
<span data-ttu-id="2fb05-121">Определяет путь к файлу, на который этот cmdlet сохраняет определение json плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="2fb05-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="2fb05-122">Определение json можно изменить для изменения плана восстановления и использовать для обновления плана восстановления с Update-AzRecoveryServicesASRRecoveryPlan-Update-AzRecoveryServicesASRRecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="2fb05-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="2fb05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb05-123">CommonParameters</span></span>
<span data-ttu-id="2fb05-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb05-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fb05-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb05-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fb05-126">INPUTS</span></span>

### <span data-ttu-id="2fb05-127">Нет</span><span class="sxs-lookup"><span data-stu-id="2fb05-127">None</span></span>

## <span data-ttu-id="2fb05-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2fb05-128">OUTPUTS</span></span>

### <span data-ttu-id="2fb05-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2fb05-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="2fb05-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2fb05-130">NOTES</span></span>

## <span data-ttu-id="2fb05-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fb05-131">RELATED LINKS</span></span>

[<span data-ttu-id="2fb05-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2fb05-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2fb05-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2fb05-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2fb05-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2fb05-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)

---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557116"
---
# <span data-ttu-id="71352-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71352-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="71352-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71352-102">SYNOPSIS</span></span>
<span data-ttu-id="71352-103">Обновляет план восстановления при восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="71352-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71352-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71352-104">SYNTAX</span></span>

### <span data-ttu-id="71352-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71352-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71352-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="71352-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71352-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71352-107">DESCRIPTION</span></span>
<span data-ttu-id="71352-108">Командлет **Update-AzureRmSiteRecoveryRecoveryPlan** обновляет план восстановления в Azure Site Recovery и публикует его.</span><span class="sxs-lookup"><span data-stu-id="71352-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="71352-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71352-109">EXAMPLES</span></span>

### <span data-ttu-id="71352-110">Пример 1: Обновление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="71352-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="71352-111">Эта команда обновляет указанный план восстановления и публикует его.</span><span class="sxs-lookup"><span data-stu-id="71352-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="71352-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71352-112">PARAMETERS</span></span>

### <span data-ttu-id="71352-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71352-113">-DefaultProfile</span></span>
<span data-ttu-id="71352-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71352-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71352-115">-Path</span><span class="sxs-lookup"><span data-stu-id="71352-115">-Path</span></span>
<span data-ttu-id="71352-116">Задает путь к файлу плана восстановления для плана восстановления, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="71352-116">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71352-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71352-117">-RecoveryPlan</span></span>
<span data-ttu-id="71352-118">Указывает план восстановления, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="71352-118">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71352-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71352-119">CommonParameters</span></span>
<span data-ttu-id="71352-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71352-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71352-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71352-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71352-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71352-122">INPUTS</span></span>

### <span data-ttu-id="71352-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71352-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="71352-124">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="71352-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="71352-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71352-125">OUTPUTS</span></span>

## <span data-ttu-id="71352-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="71352-126">NOTES</span></span>

## <span data-ttu-id="71352-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71352-127">RELATED LINKS</span></span>

[<span data-ttu-id="71352-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71352-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="71352-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71352-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="71352-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="71352-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)



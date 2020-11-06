---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 3d4530090bc1386a34056b315c79a826be5d771f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565123"
---
# <span data-ttu-id="406c6-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="406c6-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="406c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="406c6-102">SYNOPSIS</span></span>
<span data-ttu-id="406c6-103">Удаляет структуру восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="406c6-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="406c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="406c6-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="406c6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="406c6-105">DESCRIPTION</span></span>
<span data-ttu-id="406c6-106">Командлет **Remove-AzureRmSiteRecoveryFabric** удаляет структуру восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="406c6-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="406c6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="406c6-107">EXAMPLES</span></span>

## <span data-ttu-id="406c6-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="406c6-108">PARAMETERS</span></span>

### <span data-ttu-id="406c6-109">-Fabric</span><span class="sxs-lookup"><span data-stu-id="406c6-109">-Fabric</span></span>
<span data-ttu-id="406c6-110">Указывает объект структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="406c6-110">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="406c6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="406c6-111">-Force</span></span>
<span data-ttu-id="406c6-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="406c6-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406c6-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="406c6-113">-Confirm</span></span>
<span data-ttu-id="406c6-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="406c6-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406c6-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406c6-115">-WhatIf</span></span>
<span data-ttu-id="406c6-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="406c6-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="406c6-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="406c6-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406c6-118">-DefaultProfile</span></span>
<span data-ttu-id="406c6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="406c6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406c6-120">CommonParameters</span></span>
<span data-ttu-id="406c6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="406c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406c6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="406c6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406c6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="406c6-123">INPUTS</span></span>

### <span data-ttu-id="406c6-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="406c6-124">ASRFabric</span></span>
<span data-ttu-id="406c6-125">Параметр "Fabric" принимает значение типа "ASRFabric" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="406c6-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="406c6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="406c6-126">OUTPUTS</span></span>

### <span data-ttu-id="406c6-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="406c6-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="406c6-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="406c6-128">NOTES</span></span>

## <span data-ttu-id="406c6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="406c6-129">RELATED LINKS</span></span>

[<span data-ttu-id="406c6-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="406c6-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="406c6-131">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="406c6-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

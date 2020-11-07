---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733616"
---
# <span data-ttu-id="6868c-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6868c-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="6868c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6868c-102">SYNOPSIS</span></span>
<span data-ttu-id="6868c-103">Получение хранилища для восстановления сайта из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="6868c-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6868c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6868c-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6868c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6868c-105">DESCRIPTION</span></span>
<span data-ttu-id="6868c-106">Командлет **Get-AzureRmSiteRecoveryVault** получает список хранилищ Azure Site Recovery или определенное хранилище для восстановления сайта из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="6868c-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="6868c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6868c-107">EXAMPLES</span></span>

## <span data-ttu-id="6868c-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6868c-108">PARAMETERS</span></span>

### <span data-ttu-id="6868c-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6868c-109">-Name</span></span>
<span data-ttu-id="6868c-110">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="6868c-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6868c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6868c-111">-ResourceGroupName</span></span>
<span data-ttu-id="6868c-112">Указывает имя группы ресурсов Azure, из которой нужно получить объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6868c-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6868c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6868c-113">-DefaultProfile</span></span>
<span data-ttu-id="6868c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6868c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6868c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6868c-115">CommonParameters</span></span>
<span data-ttu-id="6868c-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6868c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6868c-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6868c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6868c-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6868c-118">INPUTS</span></span>

## <span data-ttu-id="6868c-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6868c-119">OUTPUTS</span></span>

### <span data-ttu-id="6868c-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="6868c-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="6868c-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="6868c-121">NOTES</span></span>

## <span data-ttu-id="6868c-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6868c-122">RELATED LINKS</span></span>

[<span data-ttu-id="6868c-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6868c-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="6868c-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6868c-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)

---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733972"
---
# <span data-ttu-id="76a5e-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="76a5e-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="76a5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="76a5e-103">Получение хранилища для восстановления сайта из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="76a5e-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76a5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76a5e-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a5e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="76a5e-106">Командлет **Get-AzureRmSiteRecoveryVault** получает список хранилищ Azure Site Recovery или определенное хранилище для восстановления сайта из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="76a5e-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="76a5e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76a5e-107">EXAMPLES</span></span>

## <span data-ttu-id="76a5e-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76a5e-108">PARAMETERS</span></span>

### <span data-ttu-id="76a5e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a5e-109">-DefaultProfile</span></span>
<span data-ttu-id="76a5e-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76a5e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76a5e-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76a5e-111">-Name</span></span>
<span data-ttu-id="76a5e-112">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="76a5e-112">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a5e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a5e-113">-ResourceGroupName</span></span>
<span data-ttu-id="76a5e-114">Указывает имя группы ресурсов Azure, из которой нужно получить объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="76a5e-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a5e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a5e-115">CommonParameters</span></span>
<span data-ttu-id="76a5e-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76a5e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a5e-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a5e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a5e-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76a5e-118">INPUTS</span></span>

### <span data-ttu-id="76a5e-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="76a5e-119">None</span></span>
<span data-ttu-id="76a5e-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="76a5e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76a5e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a5e-121">OUTPUTS</span></span>

### <span data-ttu-id="76a5e-122">System. Collections. Generic. List ' 1 [Microsoft. Azure. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="76a5e-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="76a5e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="76a5e-123">NOTES</span></span>

## <span data-ttu-id="76a5e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76a5e-124">RELATED LINKS</span></span>

[<span data-ttu-id="76a5e-125">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="76a5e-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="76a5e-126">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="76a5e-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)

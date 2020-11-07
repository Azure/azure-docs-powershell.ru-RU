---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732684"
---
# <span data-ttu-id="a91f5-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a91f5-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="a91f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a91f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a91f5-103">Создание хранилища служб восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="a91f5-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a91f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a91f5-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a91f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a91f5-105">DESCRIPTION</span></span>
<span data-ttu-id="a91f5-106">Командлет **New-AzureRmSiteRecoveryVault** создает хранилище служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a91f5-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="a91f5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a91f5-107">EXAMPLES</span></span>

## <span data-ttu-id="a91f5-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a91f5-108">PARAMETERS</span></span>

### <span data-ttu-id="a91f5-109">-Location</span><span class="sxs-lookup"><span data-stu-id="a91f5-109">-Location</span></span>
<span data-ttu-id="a91f5-110">Указывает имя географического расположения.</span><span class="sxs-lookup"><span data-stu-id="a91f5-110">Specifies the geographical location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a91f5-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a91f5-111">-Name</span></span>
<span data-ttu-id="a91f5-112">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="a91f5-112">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a91f5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a91f5-113">-ResourceGroupName</span></span>
<span data-ttu-id="a91f5-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a91f5-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a91f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a91f5-115">-DefaultProfile</span></span>
<span data-ttu-id="a91f5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a91f5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a91f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91f5-117">CommonParameters</span></span>
<span data-ttu-id="a91f5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a91f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91f5-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91f5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91f5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a91f5-120">INPUTS</span></span>

## <span data-ttu-id="a91f5-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a91f5-121">OUTPUTS</span></span>

## <span data-ttu-id="a91f5-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="a91f5-122">NOTES</span></span>

## <span data-ttu-id="a91f5-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a91f5-123">RELATED LINKS</span></span>

[<span data-ttu-id="a91f5-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a91f5-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="a91f5-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a91f5-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)

---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075577"
---
# <span data-ttu-id="80109-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="80109-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="80109-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80109-102">SYNOPSIS</span></span>
<span data-ttu-id="80109-103">Получает сайты Hyper-V из хранилища сайтов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="80109-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="80109-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80109-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80109-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80109-105">DESCRIPTION</span></span>
<span data-ttu-id="80109-106">Командлет **Get-AzureSiteRecoverySite** получает сайты Hyper-V в хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="80109-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="80109-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80109-107">EXAMPLES</span></span>

### <span data-ttu-id="80109-108">Пример 1: получение сайтов для восстановления</span><span class="sxs-lookup"><span data-stu-id="80109-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="80109-109">Эта команда получает сайты для восстановления для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="80109-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="80109-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80109-110">PARAMETERS</span></span>

### <span data-ttu-id="80109-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="80109-111">-Profile</span></span>
<span data-ttu-id="80109-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="80109-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80109-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80109-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80109-114">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="80109-114">-Vault</span></span>
<span data-ttu-id="80109-115">Указывает хранилище, для которого требуется получить доступ к сайтам.</span><span class="sxs-lookup"><span data-stu-id="80109-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="80109-116">Чтобы получить объект **ASRVault** , используйте командлет **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="80109-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80109-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80109-117">CommonParameters</span></span>
<span data-ttu-id="80109-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80109-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80109-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80109-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80109-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80109-120">INPUTS</span></span>

## <span data-ttu-id="80109-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80109-121">OUTPUTS</span></span>

## <span data-ttu-id="80109-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="80109-122">NOTES</span></span>

## <span data-ttu-id="80109-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80109-123">RELATED LINKS</span></span>

[<span data-ttu-id="80109-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="80109-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="80109-125">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="80109-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)



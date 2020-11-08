---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075892"
---
# <span data-ttu-id="15356-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="15356-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="15356-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15356-102">SYNOPSIS</span></span>
<span data-ttu-id="15356-103">Создает сайт восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="15356-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="15356-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15356-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="15356-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15356-105">DESCRIPTION</span></span>
<span data-ttu-id="15356-106">Командлет **New-AzureSiteRecoverySite** создает сайт Azure Site Recovery в текущем хранилище.</span><span class="sxs-lookup"><span data-stu-id="15356-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="15356-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15356-107">EXAMPLES</span></span>

### <span data-ttu-id="15356-108">Пример 1: создание сайта восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="15356-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="15356-109">Эта команда создает сайт восстановления сайта с именем RecoverySite07.</span><span class="sxs-lookup"><span data-stu-id="15356-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="15356-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15356-110">PARAMETERS</span></span>

### <span data-ttu-id="15356-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15356-111">-Name</span></span>
<span data-ttu-id="15356-112">Указывает имя сайта.</span><span class="sxs-lookup"><span data-stu-id="15356-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15356-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="15356-113">-Profile</span></span>
<span data-ttu-id="15356-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="15356-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15356-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15356-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="15356-116">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="15356-116">-Vault</span></span>
<span data-ttu-id="15356-117">Указывает хранилище, для которого нужно создать сайт.</span><span class="sxs-lookup"><span data-stu-id="15356-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="15356-118">Чтобы получить объект **ASRVault** , используйте командлет **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="15356-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="15356-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15356-119">CommonParameters</span></span>
<span data-ttu-id="15356-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15356-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15356-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15356-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15356-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15356-122">INPUTS</span></span>

## <span data-ttu-id="15356-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15356-123">OUTPUTS</span></span>

## <span data-ttu-id="15356-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="15356-124">NOTES</span></span>

## <span data-ttu-id="15356-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15356-125">RELATED LINKS</span></span>

[<span data-ttu-id="15356-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="15356-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="15356-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="15356-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)



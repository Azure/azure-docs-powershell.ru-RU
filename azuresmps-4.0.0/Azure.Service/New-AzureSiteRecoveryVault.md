---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075974"
---
# <span data-ttu-id="e8dda-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e8dda-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="e8dda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8dda-102">SYNOPSIS</span></span>
<span data-ttu-id="e8dda-103">Создание хранилища служб восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e8dda-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="e8dda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8dda-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8dda-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8dda-105">DESCRIPTION</span></span>
<span data-ttu-id="e8dda-106">Командлет **New-AzureSiteRecoveryVault** создает хранилище служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e8dda-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="e8dda-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8dda-107">EXAMPLES</span></span>

### <span data-ttu-id="e8dda-108">Пример 1: создание хранилища</span><span class="sxs-lookup"><span data-stu-id="e8dda-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="e8dda-109">Эта команда создает хранилище с именем ContosoVault в области "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="e8dda-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="e8dda-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8dda-110">PARAMETERS</span></span>

### <span data-ttu-id="e8dda-111">-Location</span><span class="sxs-lookup"><span data-stu-id="e8dda-111">-Location</span></span>
<span data-ttu-id="e8dda-112">Указывает географическое расположение.</span><span class="sxs-lookup"><span data-stu-id="e8dda-112">Specifies the geographical location.</span></span>

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

### <span data-ttu-id="e8dda-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8dda-113">-Name</span></span>
<span data-ttu-id="e8dda-114">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="e8dda-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="e8dda-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e8dda-115">-Profile</span></span>
<span data-ttu-id="e8dda-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e8dda-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8dda-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8dda-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e8dda-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8dda-118">CommonParameters</span></span>
<span data-ttu-id="e8dda-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8dda-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8dda-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8dda-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8dda-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8dda-121">INPUTS</span></span>

## <span data-ttu-id="e8dda-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8dda-122">OUTPUTS</span></span>

## <span data-ttu-id="e8dda-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8dda-123">NOTES</span></span>

## <span data-ttu-id="e8dda-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8dda-124">RELATED LINKS</span></span>

[<span data-ttu-id="e8dda-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e8dda-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)



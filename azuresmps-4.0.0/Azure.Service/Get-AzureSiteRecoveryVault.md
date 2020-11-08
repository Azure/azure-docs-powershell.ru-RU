---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076565"
---
# <span data-ttu-id="ecf57-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ecf57-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="ecf57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecf57-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf57-103">Получение хранилища для восстановления сайта из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ecf57-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="ecf57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecf57-104">SYNTAX</span></span>

### <span data-ttu-id="ecf57-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecf57-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ecf57-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ecf57-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ecf57-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf57-107">DESCRIPTION</span></span>
<span data-ttu-id="ecf57-108">Командлет **Get-AzureSiteRecoveryVault** получает список хранилищ Azure Site Recovery или определенное хранилище для восстановления сайта из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ecf57-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="ecf57-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecf57-109">EXAMPLES</span></span>

### <span data-ttu-id="ecf57-110">Пример 1: получение активного хранилища</span><span class="sxs-lookup"><span data-stu-id="ecf57-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="ecf57-111">Эта команда получает активное хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ecf57-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ecf57-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecf57-112">PARAMETERS</span></span>

### <span data-ttu-id="ecf57-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ecf57-113">-Name</span></span>
<span data-ttu-id="ecf57-114">Указывает имя хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ecf57-114">Specifies the name of the vault to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf57-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="ecf57-115">-Profile</span></span>
<span data-ttu-id="ecf57-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ecf57-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ecf57-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ecf57-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ecf57-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf57-118">CommonParameters</span></span>
<span data-ttu-id="ecf57-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecf57-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf57-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf57-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf57-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecf57-121">INPUTS</span></span>

## <span data-ttu-id="ecf57-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf57-122">OUTPUTS</span></span>

## <span data-ttu-id="ecf57-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecf57-123">NOTES</span></span>

## <span data-ttu-id="ecf57-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecf57-124">RELATED LINKS</span></span>

[<span data-ttu-id="ecf57-125">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ecf57-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)



---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076566"
---
# <span data-ttu-id="7779e-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="7779e-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="7779e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7779e-102">SYNOPSIS</span></span>
<span data-ttu-id="7779e-103">Получает параметры для хранилища сайта.</span><span class="sxs-lookup"><span data-stu-id="7779e-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="7779e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7779e-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7779e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7779e-105">DESCRIPTION</span></span>
<span data-ttu-id="7779e-106">Командлет **Get-AzureSiteRecoveryVaultSettings** получает параметры, связанные с текущим хранилищем Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7779e-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7779e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7779e-107">EXAMPLES</span></span>

### <span data-ttu-id="7779e-108">Пример 1: получение сведений о параметрах</span><span class="sxs-lookup"><span data-stu-id="7779e-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="7779e-109">Эта команда получает сведения о параметрах для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7779e-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7779e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7779e-110">PARAMETERS</span></span>

### <span data-ttu-id="7779e-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="7779e-111">-Profile</span></span>
<span data-ttu-id="7779e-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7779e-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7779e-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7779e-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7779e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7779e-114">CommonParameters</span></span>
<span data-ttu-id="7779e-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7779e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7779e-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7779e-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7779e-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7779e-117">INPUTS</span></span>

## <span data-ttu-id="7779e-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7779e-118">OUTPUTS</span></span>

## <span data-ttu-id="7779e-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="7779e-119">NOTES</span></span>

## <span data-ttu-id="7779e-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7779e-120">RELATED LINKS</span></span>

[<span data-ttu-id="7779e-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7779e-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="7779e-122">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7779e-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)



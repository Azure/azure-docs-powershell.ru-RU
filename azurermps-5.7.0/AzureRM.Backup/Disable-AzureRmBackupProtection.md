---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: cd3f5520b688d5a83cae20216fac47e9120b4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733584"
---
# <span data-ttu-id="cfc89-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="cfc89-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="cfc89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfc89-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc89-103">Отключает защиту для элемента, защищенного с помощью резервной копии.</span><span class="sxs-lookup"><span data-stu-id="cfc89-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfc89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfc89-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfc89-105">DESCRIPTION</span></span>
<span data-ttu-id="cfc89-106">Командлет **Disable-AzureRmBackupProtection** отключает защиту защищенного элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc89-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="cfc89-107">Этот командлет прекращает обычную архивацию элемента по расписанию.</span><span class="sxs-lookup"><span data-stu-id="cfc89-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="cfc89-108">Этот командлет может удалить существующие точки восстановления для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="cfc89-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="cfc89-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfc89-109">EXAMPLES</span></span>

## <span data-ttu-id="cfc89-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfc89-110">PARAMETERS</span></span>

### <span data-ttu-id="cfc89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc89-111">-DefaultProfile</span></span>
<span data-ttu-id="cfc89-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cfc89-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfc89-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cfc89-113">-Force</span></span>
<span data-ttu-id="cfc89-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cfc89-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-115">-Item</span><span class="sxs-lookup"><span data-stu-id="cfc89-115">-Item</span></span>
<span data-ttu-id="cfc89-116">Указывает элемент резервного копирования, для которого этот командлет отключает защиту.</span><span class="sxs-lookup"><span data-stu-id="cfc89-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="cfc89-117">Чтобы получить **AzureRmBackupItem** , используйте командлет Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="cfc89-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="cfc89-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="cfc89-119">Указывает на то, что этот командлет удаляет существующие точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc89-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="cfc89-120">Чтобы позднее удалить сохраненные точки восстановления, повторно запустите этот командлет и укажите этот параметр.</span><span class="sxs-lookup"><span data-stu-id="cfc89-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfc89-121">-Confirm</span></span>
<span data-ttu-id="cfc89-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cfc89-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc89-123">-WhatIf</span></span>
<span data-ttu-id="cfc89-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cfc89-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfc89-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cfc89-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc89-126">CommonParameters</span></span>
<span data-ttu-id="cfc89-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfc89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc89-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc89-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc89-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfc89-129">INPUTS</span></span>

### <span data-ttu-id="cfc89-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cfc89-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="cfc89-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfc89-131">OUTPUTS</span></span>

### <span data-ttu-id="cfc89-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="cfc89-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="cfc89-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfc89-133">NOTES</span></span>

## <span data-ttu-id="cfc89-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfc89-134">RELATED LINKS</span></span>

[<span data-ttu-id="cfc89-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="cfc89-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="cfc89-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cfc89-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)



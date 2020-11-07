---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: e25cbbeb4f9920e468638bbae2ef8c53ca241fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732232"
---
# <span data-ttu-id="9a437-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9a437-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="9a437-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a437-102">SYNOPSIS</span></span>
<span data-ttu-id="9a437-103">Отключает защиту для элемента, защищенного с помощью резервной копии.</span><span class="sxs-lookup"><span data-stu-id="9a437-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a437-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a437-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a437-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a437-105">DESCRIPTION</span></span>
<span data-ttu-id="9a437-106">Командлет **Disable-AzureRmBackupProtection** отключает защиту защищенного элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="9a437-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="9a437-107">Этот командлет прекращает обычную архивацию элемента по расписанию.</span><span class="sxs-lookup"><span data-stu-id="9a437-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="9a437-108">Этот командлет может удалить существующие точки восстановления для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9a437-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="9a437-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a437-109">EXAMPLES</span></span>

## <span data-ttu-id="9a437-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a437-110">PARAMETERS</span></span>

### <span data-ttu-id="9a437-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9a437-111">-Force</span></span>
<span data-ttu-id="9a437-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a437-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9a437-113">-Item</span><span class="sxs-lookup"><span data-stu-id="9a437-113">-Item</span></span>
<span data-ttu-id="9a437-114">Указывает элемент резервного копирования, для которого этот командлет отключает защиту.</span><span class="sxs-lookup"><span data-stu-id="9a437-114">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="9a437-115">Чтобы получить **AzureRmBackupItem** , используйте командлет Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="9a437-115">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a437-116">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="9a437-116">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="9a437-117">Указывает на то, что этот командлет удаляет существующие точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="9a437-117">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="9a437-118">Чтобы позднее удалить сохраненные точки восстановления, повторно запустите этот командлет и укажите этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9a437-118">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a437-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a437-119">-Confirm</span></span>
<span data-ttu-id="9a437-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a437-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a437-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a437-121">-WhatIf</span></span>
<span data-ttu-id="9a437-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a437-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a437-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a437-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a437-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a437-124">-DefaultProfile</span></span>
<span data-ttu-id="9a437-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a437-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a437-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a437-126">CommonParameters</span></span>
<span data-ttu-id="9a437-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a437-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a437-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a437-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a437-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a437-129">INPUTS</span></span>

### <span data-ttu-id="9a437-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="9a437-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="9a437-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a437-131">OUTPUTS</span></span>

### <span data-ttu-id="9a437-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9a437-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="9a437-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a437-133">NOTES</span></span>

## <span data-ttu-id="9a437-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a437-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a437-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9a437-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="9a437-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="9a437-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)



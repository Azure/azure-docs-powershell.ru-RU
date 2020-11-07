---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: d3e7a04f292be8e83bc28456c0510450c078a777
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914990"
---
# <span data-ttu-id="28790-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28790-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="28790-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28790-102">SYNOPSIS</span></span>
<span data-ttu-id="28790-103">Удаление учетной записи хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="28790-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28790-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28790-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28790-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28790-105">DESCRIPTION</span></span>
<span data-ttu-id="28790-106">Командлет **Remove-AzureRmStorageAccount** удаляет учетную запись хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="28790-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="28790-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28790-107">EXAMPLES</span></span>

### <span data-ttu-id="28790-108">Пример 1: Удаление учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="28790-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="28790-109">Эта команда удаляет указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="28790-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="28790-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28790-110">PARAMETERS</span></span>

### <span data-ttu-id="28790-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28790-111">-AsJob</span></span>
<span data-ttu-id="28790-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="28790-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28790-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28790-113">-DefaultProfile</span></span>
<span data-ttu-id="28790-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28790-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28790-115">-Force</span><span class="sxs-lookup"><span data-stu-id="28790-115">-Force</span></span>
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

### <span data-ttu-id="28790-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28790-116">-Name</span></span>
<span data-ttu-id="28790-117">Указывает имя учетной записи хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="28790-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28790-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28790-118">-ResourceGroupName</span></span>
<span data-ttu-id="28790-119">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="28790-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28790-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28790-120">-Confirm</span></span>
<span data-ttu-id="28790-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28790-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28790-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28790-122">-WhatIf</span></span>
<span data-ttu-id="28790-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28790-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28790-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28790-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28790-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28790-125">CommonParameters</span></span>
<span data-ttu-id="28790-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28790-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28790-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28790-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28790-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28790-128">INPUTS</span></span>

### <span data-ttu-id="28790-129">System. String</span><span class="sxs-lookup"><span data-stu-id="28790-129">System.String</span></span>

## <span data-ttu-id="28790-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28790-130">OUTPUTS</span></span>

### <span data-ttu-id="28790-131">System. void</span><span class="sxs-lookup"><span data-stu-id="28790-131">System.Void</span></span>

## <span data-ttu-id="28790-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="28790-132">NOTES</span></span>

## <span data-ttu-id="28790-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28790-133">RELATED LINKS</span></span>

[<span data-ttu-id="28790-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28790-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="28790-135">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28790-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="28790-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28790-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)



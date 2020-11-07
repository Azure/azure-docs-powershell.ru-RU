---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913331"
---
# <span data-ttu-id="e63f5-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e63f5-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="e63f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e63f5-102">SYNOPSIS</span></span>
<span data-ttu-id="e63f5-103">Удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e63f5-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e63f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e63f5-104">SYNTAX</span></span>

### <span data-ttu-id="e63f5-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="e63f5-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63f5-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="e63f5-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e63f5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e63f5-107">DESCRIPTION</span></span>
<span data-ttu-id="e63f5-108">Командлет **Remove-AzureRmKeyVault** удаляет указанное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="e63f5-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="e63f5-109">Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="e63f5-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="e63f5-110">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="e63f5-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="e63f5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e63f5-111">EXAMPLES</span></span>

### <span data-ttu-id="e63f5-112">Пример 1: Удаление хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="e63f5-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="e63f5-113">Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="e63f5-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="e63f5-114">Пример 2: Удаление хранилища ключей из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e63f5-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="e63f5-115">Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e63f5-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="e63f5-116">Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="e63f5-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="e63f5-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e63f5-117">PARAMETERS</span></span>

### <span data-ttu-id="e63f5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e63f5-118">-AsJob</span></span>
<span data-ttu-id="e63f5-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e63f5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e63f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e63f5-120">-DefaultProfile</span></span>
<span data-ttu-id="e63f5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e63f5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e63f5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e63f5-122">-Force</span></span>
<span data-ttu-id="e63f5-123">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e63f5-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="e63f5-124">По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e63f5-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="e63f5-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e63f5-125">-InRemovedState</span></span>
<span data-ttu-id="e63f5-126">Удалить ранее удаленное хранилище без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="e63f5-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f5-127">-Location</span><span class="sxs-lookup"><span data-stu-id="e63f5-127">-Location</span></span>
<span data-ttu-id="e63f5-128">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="e63f5-128">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63f5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e63f5-129">-ResourceGroupName</span></span>
<span data-ttu-id="e63f5-130">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e63f5-130">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63f5-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e63f5-131">-VaultName</span></span>
<span data-ttu-id="e63f5-132">Указывает имя хранилища ключей, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e63f5-132">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63f5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e63f5-133">-Confirm</span></span>
<span data-ttu-id="e63f5-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e63f5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e63f5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e63f5-135">-WhatIf</span></span>
<span data-ttu-id="e63f5-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e63f5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e63f5-137">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e63f5-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e63f5-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e63f5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e63f5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e63f5-139">CommonParameters</span></span>
<span data-ttu-id="e63f5-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e63f5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e63f5-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e63f5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e63f5-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e63f5-142">INPUTS</span></span>

## <span data-ttu-id="e63f5-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e63f5-143">OUTPUTS</span></span>

## <span data-ttu-id="e63f5-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e63f5-144">NOTES</span></span>

## <span data-ttu-id="e63f5-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e63f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="e63f5-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e63f5-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="e63f5-147">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e63f5-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

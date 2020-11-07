---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911166"
---
# <span data-ttu-id="f577b-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f577b-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="f577b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f577b-102">SYNOPSIS</span></span>
<span data-ttu-id="f577b-103">Удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f577b-103">Deletes a key vault.</span></span>

## <span data-ttu-id="f577b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f577b-104">SYNTAX</span></span>

### <span data-ttu-id="f577b-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="f577b-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f577b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="f577b-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f577b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f577b-107">DESCRIPTION</span></span>
<span data-ttu-id="f577b-108">Командлет **Remove-AzKeyVault** удаляет указанное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f577b-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="f577b-109">Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="f577b-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="f577b-110">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="f577b-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="f577b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f577b-111">EXAMPLES</span></span>

### <span data-ttu-id="f577b-112">Пример 1: Удаление хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="f577b-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="f577b-113">Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="f577b-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="f577b-114">Пример 2: Удаление хранилища ключей из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f577b-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="f577b-115">Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f577b-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="f577b-116">Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f577b-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="f577b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f577b-117">PARAMETERS</span></span>

### <span data-ttu-id="f577b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f577b-118">-AsJob</span></span>
<span data-ttu-id="f577b-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f577b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f577b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f577b-120">-DefaultProfile</span></span>
<span data-ttu-id="f577b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f577b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f577b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f577b-122">-Force</span></span>
<span data-ttu-id="f577b-123">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f577b-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="f577b-124">По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f577b-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="f577b-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f577b-125">-InRemovedState</span></span>
<span data-ttu-id="f577b-126">Удалить ранее удаленное хранилище без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="f577b-126">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="f577b-127">-Location</span><span class="sxs-lookup"><span data-stu-id="f577b-127">-Location</span></span>
<span data-ttu-id="f577b-128">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f577b-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="f577b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f577b-129">-ResourceGroupName</span></span>
<span data-ttu-id="f577b-130">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f577b-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f577b-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f577b-131">-VaultName</span></span>
<span data-ttu-id="f577b-132">Указывает имя хранилища ключей, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f577b-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="f577b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f577b-133">-Confirm</span></span>
<span data-ttu-id="f577b-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f577b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f577b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f577b-135">-WhatIf</span></span>
<span data-ttu-id="f577b-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f577b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f577b-137">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f577b-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f577b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f577b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f577b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f577b-139">CommonParameters</span></span>
<span data-ttu-id="f577b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f577b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f577b-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f577b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f577b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f577b-142">INPUTS</span></span>

### <span data-ttu-id="f577b-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="f577b-143">None</span></span>
<span data-ttu-id="f577b-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f577b-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f577b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f577b-145">OUTPUTS</span></span>

## <span data-ttu-id="f577b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f577b-146">NOTES</span></span>

## <span data-ttu-id="f577b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f577b-147">RELATED LINKS</span></span>

[<span data-ttu-id="f577b-148">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f577b-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="f577b-149">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f577b-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

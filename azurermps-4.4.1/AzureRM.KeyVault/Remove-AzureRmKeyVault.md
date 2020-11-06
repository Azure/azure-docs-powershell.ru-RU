---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568052"
---
# <span data-ttu-id="54afb-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="54afb-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="54afb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54afb-102">SYNOPSIS</span></span>
<span data-ttu-id="54afb-103">Удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="54afb-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54afb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54afb-104">SYNTAX</span></span>

### <span data-ttu-id="54afb-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="54afb-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54afb-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="54afb-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54afb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54afb-107">DESCRIPTION</span></span>
<span data-ttu-id="54afb-108">Командлет **Remove-AzureRmKeyVault** удаляет указанное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="54afb-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="54afb-109">Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="54afb-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="54afb-110">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="54afb-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="54afb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54afb-111">EXAMPLES</span></span>

### <span data-ttu-id="54afb-112">Пример 1: Удаление хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="54afb-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="54afb-113">Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="54afb-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="54afb-114">Пример 2: Удаление хранилища ключей из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="54afb-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="54afb-115">Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54afb-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="54afb-116">Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="54afb-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="54afb-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54afb-117">PARAMETERS</span></span>

### <span data-ttu-id="54afb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="54afb-118">-Force</span></span>
<span data-ttu-id="54afb-119">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="54afb-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="54afb-120">По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="54afb-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="54afb-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="54afb-121">-InRemovedState</span></span>
<span data-ttu-id="54afb-122">Удалить ранее удаленное хранилище без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="54afb-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54afb-123">-Location</span><span class="sxs-lookup"><span data-stu-id="54afb-123">-Location</span></span>
<span data-ttu-id="54afb-124">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="54afb-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54afb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54afb-125">-ResourceGroupName</span></span>
<span data-ttu-id="54afb-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54afb-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54afb-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54afb-127">-VaultName</span></span>
<span data-ttu-id="54afb-128">Указывает имя хранилища ключей, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="54afb-128">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54afb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54afb-129">-Confirm</span></span>
<span data-ttu-id="54afb-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54afb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54afb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54afb-131">-WhatIf</span></span>
<span data-ttu-id="54afb-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54afb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54afb-133">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54afb-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54afb-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54afb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54afb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54afb-135">-DefaultProfile</span></span>
<span data-ttu-id="54afb-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54afb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54afb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54afb-137">CommonParameters</span></span>
<span data-ttu-id="54afb-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54afb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54afb-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54afb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54afb-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54afb-140">INPUTS</span></span>

## <span data-ttu-id="54afb-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54afb-141">OUTPUTS</span></span>

## <span data-ttu-id="54afb-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="54afb-142">NOTES</span></span>

## <span data-ttu-id="54afb-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54afb-143">RELATED LINKS</span></span>

[<span data-ttu-id="54afb-144">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="54afb-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="54afb-145">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="54afb-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

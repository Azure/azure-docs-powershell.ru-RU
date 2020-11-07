---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: fd2483925e8ab14772a3bf34d4411748583a03c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910269"
---
# <span data-ttu-id="907f4-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="907f4-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="907f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="907f4-102">SYNOPSIS</span></span>
<span data-ttu-id="907f4-103">Восстановление удаленного хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="907f4-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="907f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="907f4-104">SYNTAX</span></span>

```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="907f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="907f4-105">DESCRIPTION</span></span>
<span data-ttu-id="907f4-106">Командлет **Undo-AzKeyVaultRemoval** восстановит ранее удаленное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="907f4-106">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="907f4-107">Восстановленное хранилище станет активным после восстановления</span><span class="sxs-lookup"><span data-stu-id="907f4-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="907f4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="907f4-108">EXAMPLES</span></span>

### <span data-ttu-id="907f4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="907f4-109">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="907f4-110">Эта команда восстанавливает активное и пригодное состояние для хранилища ключей "MyKeyVault", который ранее был удален из группы ресурсов eastus2 Region и "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="907f4-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="907f4-111">Он также заменяет Теги на новый тег.</span><span class="sxs-lookup"><span data-stu-id="907f4-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="907f4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="907f4-112">PARAMETERS</span></span>

### <span data-ttu-id="907f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907f4-113">-DefaultProfile</span></span>
<span data-ttu-id="907f4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="907f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="907f4-115">-Location</span><span class="sxs-lookup"><span data-stu-id="907f4-115">-Location</span></span>
<span data-ttu-id="907f4-116">Указывает исходный регион для удаленного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="907f4-116">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="907f4-118">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="907f4-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="907f4-119">-Tag</span></span>
<span data-ttu-id="907f4-120">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="907f4-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="907f4-121">Например:</span><span class="sxs-lookup"><span data-stu-id="907f4-121">For example:</span></span>

<span data-ttu-id="907f4-122">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="907f4-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="907f4-123">-VaultName</span></span>
<span data-ttu-id="907f4-124">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="907f4-124">Vault name.</span></span>
<span data-ttu-id="907f4-125">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="907f4-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="907f4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="907f4-126">-Confirm</span></span>
<span data-ttu-id="907f4-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="907f4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907f4-128">-WhatIf</span></span>
<span data-ttu-id="907f4-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="907f4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="907f4-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="907f4-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907f4-131">CommonParameters</span></span>
<span data-ttu-id="907f4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="907f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907f4-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907f4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907f4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="907f4-134">INPUTS</span></span>

### <span data-ttu-id="907f4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="907f4-135">System.String</span></span>
<span data-ttu-id="907f4-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="907f4-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="907f4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="907f4-137">OUTPUTS</span></span>

### <span data-ttu-id="907f4-138">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="907f4-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="907f4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="907f4-139">NOTES</span></span>

## <span data-ttu-id="907f4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="907f4-140">RELATED LINKS</span></span>

[<span data-ttu-id="907f4-141">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="907f4-141">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="907f4-142">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="907f4-142">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="907f4-143">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="907f4-143">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

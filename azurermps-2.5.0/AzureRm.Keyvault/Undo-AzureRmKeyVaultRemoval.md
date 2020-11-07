---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
ms.openlocfilehash: a557676d35eb167438f29c36a729ee652a45d591
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913869"
---
# <span data-ttu-id="d83bb-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="d83bb-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="d83bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d83bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d83bb-103">Восстановление удаленного хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="d83bb-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d83bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d83bb-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d83bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d83bb-105">DESCRIPTION</span></span>
<span data-ttu-id="d83bb-106">Командлет **Undo-AzureRmKeyVaultRemoval** восстановит ранее удаленное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="d83bb-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="d83bb-107">Восстановленное хранилище станет активным после восстановления</span><span class="sxs-lookup"><span data-stu-id="d83bb-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="d83bb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d83bb-108">EXAMPLES</span></span>

### <span data-ttu-id="d83bb-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d83bb-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="d83bb-110">Эта команда восстанавливает активное и пригодное состояние для хранилища ключей "MyKeyVault", который ранее был удален из группы ресурсов eastus2 Region и "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d83bb-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="d83bb-111">Он также заменяет Теги на новый тег.</span><span class="sxs-lookup"><span data-stu-id="d83bb-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="d83bb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d83bb-112">PARAMETERS</span></span>

### <span data-ttu-id="d83bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83bb-113">-DefaultProfile</span></span>
<span data-ttu-id="d83bb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d83bb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d83bb-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d83bb-115">-Location</span></span>
<span data-ttu-id="d83bb-116">Указывает исходный регион для удаленного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d83bb-116">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="d83bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d83bb-118">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="d83bb-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="d83bb-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="d83bb-119">-Tag</span></span>
<span data-ttu-id="d83bb-120">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="d83bb-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d83bb-121">Например:</span><span class="sxs-lookup"><span data-stu-id="d83bb-121">For example:</span></span>

<span data-ttu-id="d83bb-122">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="d83bb-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d83bb-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d83bb-123">-VaultName</span></span>
<span data-ttu-id="d83bb-124">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="d83bb-124">Vault name.</span></span>
<span data-ttu-id="d83bb-125">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="d83bb-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d83bb-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d83bb-126">-Confirm</span></span>
<span data-ttu-id="d83bb-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d83bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d83bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d83bb-128">-WhatIf</span></span>
<span data-ttu-id="d83bb-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d83bb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d83bb-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d83bb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d83bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83bb-131">CommonParameters</span></span>
<span data-ttu-id="d83bb-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d83bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83bb-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83bb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83bb-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d83bb-134">INPUTS</span></span>

### <span data-ttu-id="d83bb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d83bb-135">System.String</span></span>
<span data-ttu-id="d83bb-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d83bb-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d83bb-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d83bb-137">OUTPUTS</span></span>

### <span data-ttu-id="d83bb-138">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="d83bb-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="d83bb-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d83bb-139">NOTES</span></span>

## <span data-ttu-id="d83bb-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d83bb-140">RELATED LINKS</span></span>

[<span data-ttu-id="d83bb-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d83bb-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="d83bb-142">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d83bb-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="d83bb-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d83bb-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733721"
---
# <span data-ttu-id="902e6-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="902e6-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="902e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="902e6-102">SYNOPSIS</span></span>
<span data-ttu-id="902e6-103">Восстановление удаленного хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="902e6-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="902e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="902e6-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="902e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="902e6-105">DESCRIPTION</span></span>
<span data-ttu-id="902e6-106">Командлет **Undo-AzureRmKeyVaultRemoval** восстановит ранее удаленное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="902e6-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="902e6-107">Восстановленное хранилище станет активным после восстановления</span><span class="sxs-lookup"><span data-stu-id="902e6-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="902e6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="902e6-108">EXAMPLES</span></span>

### <span data-ttu-id="902e6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="902e6-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="902e6-110">Эта команда восстанавливает активное и пригодное состояние для хранилища ключей "MyKeyVault", который ранее был удален из группы ресурсов eastus2 Region и "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="902e6-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="902e6-111">Он также заменяет Теги на новый тег.</span><span class="sxs-lookup"><span data-stu-id="902e6-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="902e6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="902e6-112">PARAMETERS</span></span>

### <span data-ttu-id="902e6-113">-Location</span><span class="sxs-lookup"><span data-stu-id="902e6-113">-Location</span></span>
<span data-ttu-id="902e6-114">Указывает исходный регион для удаленного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="902e6-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902e6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="902e6-115">-ResourceGroupName</span></span>
<span data-ttu-id="902e6-116">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="902e6-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="902e6-117">-Тег</span><span class="sxs-lookup"><span data-stu-id="902e6-117">-Tag</span></span>
<span data-ttu-id="902e6-118">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="902e6-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="902e6-119">Например:</span><span class="sxs-lookup"><span data-stu-id="902e6-119">For example:</span></span>

<span data-ttu-id="902e6-120">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="902e6-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902e6-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="902e6-121">-VaultName</span></span>
<span data-ttu-id="902e6-122">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="902e6-122">Vault name.</span></span>
<span data-ttu-id="902e6-123">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="902e6-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="902e6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="902e6-124">-Confirm</span></span>
<span data-ttu-id="902e6-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="902e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="902e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="902e6-126">-WhatIf</span></span>
<span data-ttu-id="902e6-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="902e6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="902e6-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="902e6-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="902e6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902e6-129">-DefaultProfile</span></span>
<span data-ttu-id="902e6-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="902e6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="902e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902e6-131">CommonParameters</span></span>
<span data-ttu-id="902e6-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="902e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902e6-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="902e6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902e6-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="902e6-134">INPUTS</span></span>

### <span data-ttu-id="902e6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="902e6-135">System.String</span></span>
<span data-ttu-id="902e6-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="902e6-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="902e6-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="902e6-137">OUTPUTS</span></span>

### <span data-ttu-id="902e6-138">Microsoft. Azure. Commands. KeyVault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="902e6-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="902e6-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="902e6-139">NOTES</span></span>

## <span data-ttu-id="902e6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="902e6-140">RELATED LINKS</span></span>

[<span data-ttu-id="902e6-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="902e6-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="902e6-142">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="902e6-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="902e6-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="902e6-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

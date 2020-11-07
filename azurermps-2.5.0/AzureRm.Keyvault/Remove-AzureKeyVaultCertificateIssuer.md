---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913339"
---
# <span data-ttu-id="293d5-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="293d5-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="293d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="293d5-102">SYNOPSIS</span></span>
<span data-ttu-id="293d5-103">Удаление поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="293d5-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="293d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="293d5-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="293d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="293d5-105">DESCRIPTION</span></span>
<span data-ttu-id="293d5-106">Командлет **Remove-AzureKeyVaultCertificateIssuer** Удаляет поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="293d5-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="293d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="293d5-107">EXAMPLES</span></span>

### <span data-ttu-id="293d5-108">Пример 1: Удаление поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="293d5-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="293d5-109">Эта команда удаляет издателя сертификата с именем TestIssuer01 из хранилища ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="293d5-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="293d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="293d5-110">PARAMETERS</span></span>

### <span data-ttu-id="293d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293d5-111">-DefaultProfile</span></span>
<span data-ttu-id="293d5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="293d5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="293d5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="293d5-113">-Force</span></span>
<span data-ttu-id="293d5-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="293d5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="293d5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="293d5-115">-Name</span></span>
<span data-ttu-id="293d5-116">Указывает имя поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="293d5-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293d5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="293d5-117">-PassThru</span></span>
<span data-ttu-id="293d5-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="293d5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="293d5-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="293d5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="293d5-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="293d5-120">-VaultName</span></span>
<span data-ttu-id="293d5-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="293d5-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="293d5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="293d5-122">-Confirm</span></span>
<span data-ttu-id="293d5-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="293d5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="293d5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="293d5-124">-WhatIf</span></span>
<span data-ttu-id="293d5-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="293d5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="293d5-126">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="293d5-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="293d5-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="293d5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="293d5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293d5-128">CommonParameters</span></span>
<span data-ttu-id="293d5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="293d5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293d5-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293d5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293d5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="293d5-131">INPUTS</span></span>

## <span data-ttu-id="293d5-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="293d5-132">OUTPUTS</span></span>

### <span data-ttu-id="293d5-133">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="293d5-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="293d5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="293d5-134">NOTES</span></span>

## <span data-ttu-id="293d5-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="293d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="293d5-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="293d5-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="293d5-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="293d5-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)



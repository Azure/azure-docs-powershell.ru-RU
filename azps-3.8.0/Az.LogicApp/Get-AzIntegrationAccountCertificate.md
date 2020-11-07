---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912228"
---
# <span data-ttu-id="a211e-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a211e-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="a211e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a211e-102">SYNOPSIS</span></span>
<span data-ttu-id="a211e-103">Получает сертификаты учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a211e-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="a211e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a211e-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a211e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a211e-105">DESCRIPTION</span></span>
<span data-ttu-id="a211e-106">Командлет **Get-AzIntegrationAccountCertificate** получает сертификаты учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a211e-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="a211e-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="a211e-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="a211e-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a211e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a211e-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="a211e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a211e-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a211e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a211e-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a211e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a211e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a211e-112">EXAMPLES</span></span>

### <span data-ttu-id="a211e-113">Пример 1: получение сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="a211e-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="a211e-114">Эта команда получает сертификат учетной записи интеграции с именем IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="a211e-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="a211e-115">Пример 2: получение сертификатов учетной записи интеграции по имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="a211e-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="a211e-116">Эта команда получает сертификаты учетной записи интеграции для учетной записи интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="a211e-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="a211e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a211e-117">PARAMETERS</span></span>

### <span data-ttu-id="a211e-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a211e-118">-CertificateName</span></span>
<span data-ttu-id="a211e-119">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a211e-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a211e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a211e-120">-DefaultProfile</span></span>
<span data-ttu-id="a211e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a211e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a211e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a211e-122">-Name</span></span>
<span data-ttu-id="a211e-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a211e-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a211e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a211e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a211e-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a211e-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a211e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a211e-126">CommonParameters</span></span>
<span data-ttu-id="a211e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a211e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a211e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a211e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a211e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a211e-129">INPUTS</span></span>

### <span data-ttu-id="a211e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a211e-130">System.String</span></span>

## <span data-ttu-id="a211e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a211e-131">OUTPUTS</span></span>

### <span data-ttu-id="a211e-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a211e-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="a211e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a211e-133">NOTES</span></span>

## <span data-ttu-id="a211e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a211e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a211e-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a211e-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="a211e-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a211e-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="a211e-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a211e-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


